Python version 10.0
(Испльзовались match-case)


Для того чтобы создать программу с расширением .exe -->
Необходимо скопировать и выполнить в консоли:

1) Установка PyInstaller
$ python3 -m pip install pyinstaller

2) Установка дополнительных библиотек для Python 3.10
$ python3 -m pip install https://github.com/rokm/pyinstaller/archive/refs/heads/python-3.10.zip

3) Проходит компиляция кода
$ python3 -m PyInstaller --onefile 'tree_covid19.py'


PyInstaller собирает в один пакет Python-приложение и все необходимые ему библиотеки следующим образом:
- Считывает файл скрипта.
- Анализирует код для выявления всех зависимостей, необходимых для работы.
- Создает файл spec, который содержит название скрипта, библиотеки-зависимости, любые файлы, включая те параметры, которые были переданы в команду PyInstaller.
- Собирает копии всех библиотек и файлов вместе с активным интерпретатором Python.
- Создает папку BUILD в папке со скриптом и записывает логи вместе с рабочими файлами в BUILD.
- Создает папку DIST в папке со скриптом, если она еще не существует.
- Записывает все необходимые файлы вместе со скриптом или в одну папку, или в один исполняемый файл.