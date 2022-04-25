https://proglib.io/p/kak-sdelat-sayt-na-python-za-5-minut-s-pomoshchyu-ssg-generatora-pelican-2022-04-18
https://docs.getpelican.com/en/stable/pelican-themes.html

mkdir e:\myblog
cd e:\myblog
mkdir .venv
pipenv install pelican[Markdown]
pipenv shell
pelican-quickstart


Пеликан автоматически создает две папки – content и output. В первой папке пользователь сохраняет посты, страницы и изображения, во вторую генератор выгружает готовые html-страницы. Посты нужно сохранять в поддиректории articles, страницы – в pages, изображения – в images. Поддиректории придется создать вручную.

Для генерации сайта нужно положить в папку content\articles хотя бы один Markdown файл. 


pelican content

Запустить сервер можно тремя способами:

    pelican --listen – стандартный;
    pelican -l – сокращенный;
    pelican -r -l – с автоматической регенерацией контента (используется в режиме разработки – для кастомизации темы, тестирования плагинов и так далее). Команду запуска можно комбинировать с командой генерации контента: pelican content -l.

Сайт будет доступен в браузере по адресу http://localhost:8000/.


Смена темы:
https://github.com/getpelican/pelican-themes

 .venv\Lib\site-packages\pelican\themes, а в конфигурационном файле указать название темы:

THEME = 'flex'

pelican content -r -l,


+++++++++++++++++++++++++++++++++++++++++
 python -m venv env
.\env\Scripts\activate
pip install pelican[Markdown]






