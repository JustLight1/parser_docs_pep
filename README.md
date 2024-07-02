<div align=center>
    
# Парсер документации python

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

</div>

## Описание проекта

Данный парсер умеет:

1. Собирать данные обо всех документах PEP.
2. Сравнивать статус на странице PEP со статусом в общем списке и в случае разницы выводить в логи.
3. Считать количество PEP в каждом статусе и общее количество PEP.
4. Выводить результат в консоль в обычном формате, в виде таблицы или в файл csv.

## Технологии

- Python 3.10.11
- beautifulsoup4 4.12.3
- tqdm 4.66.4
- prettytable 2.1.0

## Запуск проекта

1. Cклонировать проект:

```bash
git clone git@github.com:JustLight1/parser_docs_pep.git
```

2. Создать виртуальное окружение и активировать:

```bash
python -m venv venv
source venv/Scripts/activate - windows
```

3. Установить библиотеки из файла requirements.txt:

```bash
pip install -r requirements.txt
```

4. Перейти в директорию src для дальнейшей работы:

```bash
cd src/
```

## Пример работы парсера

Парсер может работать в разных режимах с разными аргументами:

```bash
usage: main.py [-h] [-c] [-o {pretty,file}]
               {whats-new,latest-versions,download,pep}
```

1. Режимы работы парсера:

   positional arguments:
   whats-new - Парсинг новостей
   latest-versions - Парсинг версий
   download - Загрузка архива с документацией в формате pdf
   pep - Парсинг PEP

2. Дополнительные аргументы:

   optional arguments:
   -h, --help "show this help message and exit"
   -c, --clear-cache "Очистка кеша"
   -o {pretty,file}, --output {pretty,file} "Дополнительные способы вывода данных"
