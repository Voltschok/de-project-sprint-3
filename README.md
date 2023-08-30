# Проект 3-го спринта

### Описание
В проекте по обновлению пайплайна обработки данных (de-project-sprint-3) было реализовано получение инкремента данных через API, загрузка их в STG-слой БД. Обновление витрин данных было автоматизировано с помощью Airflow.

### Как работать с репозиторием
1. В вашем GitHub-аккаунте автоматически создастся репозиторий `de-project-sprint-3` после того, как вы привяжете свой GitHub-аккаунт на Платформе.
2. Скопируйте репозиторий на свой локальный компьютер, в качестве пароля укажите ваш `Access Token` (получить нужно на странице [Personal Access Tokens](https://github.com/settings/tokens)):
	* `git clone https://github.com/{{ username }}/de-project-sprint-3.git`
3. Перейдите в директорию с проектом: 
	* `cd de-project-sprint-3`
4. Выполните проект и сохраните получившийся код в локальном репозитории:
	* `git add .`
	* `git commit -m 'my best commit'`
5. Обновите репозиторий в вашем GutHub-аккаунте:
	* `git push origin main`

### Структура репозитория
1. Папка `migrations` хранит файлы миграции. Файлы миграции должны быть с расширением `.sql` и содержать SQL-скрипт обновления базы данных.
2. В папке `src` хранятся все необходимые исходники: 
    * Папка `dags` содержит DAG's Airflow.

### Как запустить контейнер
Запустите локально команду:

```
docker run -d --rm -p 3000:3000 -p 15432:5432 --name=de-project-sprint-3-server sindb/project-sprint-3:latest
```

После того как запустится контейнер, у вас будут доступны:
1. Visual Studio Code
2. Airflow
3. Database
