Отчёт по работе в `demo_repo`

1) Подготовка и инициализация репозитория
- Перешла на диск `D:` и в папку проекта: `D:\web\demo_repo`.
- Инициализировала Git-репозиторий: `git init`.
- Проверила состояние репозитория: `git status` (коммитов ещё не было).

2) Создание первого файла и первый коммит
- Создала файл `readme.txt` и добавила его в индекс: `git add readme.txt`.
- Сделала первый коммит:
  - `git commit -m "first file"`

3) Изменения и добавление нескольких `.txt` файлов одним коммитом
- Обновила содержимое `readme.txt` и добавила изменения в индекс: `git add readme.txt`.
- Создала дополнительные файлы `readme_after.txt` и `readme_now.txt`.
- Добавила все `.txt` файлы:
  - `git add "*.txt"`
- Сделала коммит со всеми `.txt` файлами:
  - `git commit -m "all files with txt extentionwere added"`
- Посмотрела историю и сводку:
  - `git log`
  - `git log --summary`

4) Подключение удалённого репозитория и отправка изменений
- Добавила remote:
  - `git remote add origin git@github.com:0Tzhbeva0/demo-repo.git`
- Отправила ветку `master`:
  - `git push -u origin master`

5) Подтягивание изменений с GitHub и просмотр diff
- Выполнила `git pull origin master` и получила обновление `readme.txt`.
- Посмотрела отличия:
  - `git diff HEAD`

6) Эксперименты с папкой и индексом (staging) + откат
- Создала папку `folder` и файл `folder/bye.txt`.
- Добавила файл в индекс:
  - `git add folder/bye.txt`
- Затем убрал файл из индекса (unstage):
  - `git reset folder/bye.txt`
- Проверяла изменения:
  - `git diff --staged`
  - `git diff`
- Откатила изменения в `readme.txt`:
  - `git checkout -- readme.txt`

7) Работа с ветками и удаление файлов через отдельную ветку
- Создала ветку для “чистки” и переключилась на неё:
  - `git branch clean_up`
  - `git checkout clean_up`
- Удалила из репозитория файлы `readme_after.txt` и `readme_now.txt`:
  - `git rm readme_after.txt`
  - `git rm readme_now.txt`
- Закоммитила удаление:
  - `git commit -m "deleted folder and files"`

8) Слияние ветки и отправка результата
- Переключилась обратно на `master` и влила изменения:
  - `git checkout master`
  - `git merge clean_up`
- Удалила ветку:
  - `git branch -d clean_up`
- Отправил изменения на GitHub:
  - `git push`
