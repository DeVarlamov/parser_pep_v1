# Парсер документации Python

## 1. [Описание](#1)
## 2. [Запуск парсера](#2)
## 3. [Примеры команд](#3)
## 4. [Техническая информация](#4)
## 5. [Об авторе](#5)

---
## 1. Описание <a id=1></a>

Проект парсера позволяет получать информацию о новостях и
всех версиях Python, скачивать документацию по последней версии Python
в формате PDF(A4) и информацию по статусам и количеству PEP.

---
## 2. Запуск парсера <a id=2></a>

Перед запуском необходимо склонировать проект:
```bash
HTTPS: git clone https://github.com/DIABLik666/bs4_parser_pep.git
SSH: git clone git@github.com:DIABLik666/bs4_parser_pep.git
```

Cоздать и активировать виртуальное окружение:
```bash
python -m venv venv
```
```bash
Linux: source venv/bin/activate
Windows: source venv/Scripts/activate
```

И установить зависимости из файла requirements.txt:
```bash
python3 -m pip install --upgrade pip
```
```bash
pip install -r requirements.txt
```

### Парсер может работать в четырех режимах работы:
- whats-new
- latest-versions
- download
- pep

Для запуска парсера необходимо обязательно указать один из режимов.

### Дополнительные (не обязательные) команды парсера:
- -c, --clear-cache (Очистка кеша перед парсингом)
- -o, --output (Формат вывода)
- -h (Вызов справки)

### Вывод может быть осуществлён в трёх форматах:
- Вывод в терминал сплошного текста (при отсутствии аргумента -o)
- Вывод в терминал в виде таблицы (с аргументом -o pretty)
- Вывод в файл формата .csv (с аргументом -o file)

---
## 3. Примеры команд <a id=3></a>

Получить ссылки на последние новости по всем версиям Python в терминале (с очисткой кеша):
```bash
python src/main.py whats-new -с
```

Получить ссылки на документацию всех версий Python в виде таблицы:
```bash
python src/main.py latest-versions -o pretty
```

Cкачать документацию по последней версии Python в формате PDF(A4):
```bash
python src/main.py download
```

Получить информацию по статусам и количеству PEP с записью в файл формата csv:
```bash
python src/main.py pep -o file
```

---
## 4. Техническая информация <a id=4></a>

Стек технологий: Python, BeautifulSoup4

При выводе информации в файл (-o file) он сохраняется в папке src/results/  
Скачанная документация Python сохраняется в папке src/downloads/  
Логи работы парсера расположены в папке src/logs/

---
## 5. Об авторе <a id=5></a>

Варламов Николай Олегович 
Python-разработчик (Backend)  
Россия, г. Санкт Петербург  
E-mail: devarlamov1@yandex.ru  
Telegram: @DeVarlamov
