# everything-recognition

Данный проект в режиме реального времени отображает видео с веб-камеры, на котором распознаёт человеческие лица и прочие объекты, подсвечивая их цветными прямоугольными рамками.


## Установка

Должен быть установлен python3.
Затем используйте pip (или pip3, если есть конфликт с python2) для установки зависимостей:

```
pip install -r requirements.txt
```

или

```
pip3 install -r requirements.txt
```

Рекомендуется использовать venv для изоляции проекта.


## Запуск


### run.py

Находясь в директории проекта, откройте с помощью python3 файл `run.py`.

```
python3 run.py
```

Скрипт подключится к видео-потоку от веб-камеры, выведет его на экран и будет в режиме реального времени обозначать на нём распознаваемые объекты. 

Если не удастся обнаружить веб-камеру, скрипт выведет соответствующее сообщение.


### config.py

Здесь содержится словарь с настройками, в котором указываются пути к библиотекам для распознавания объектов, выбирается или отменяется выделение и задаётся цвет выделения для распознаваемых объектов: лиц, профилей, улыбок, глаз, тел и кошачьих мордочек.

Для изменения настроек используйте пространство значений ключей `"path"`, `"color"` и `"draw"`.

По аналогии можно подключить и прочие библиотеки, находящиеся в папке `haarcascades`, указав к ним путь, выбрав цвет рамок и поставив значение `"draw": True`.


### haarcascades

В этой директории находятся библиотеки `banana_classifier.xml` и `cars.xml`, а также папки `faces` и `road-signs`, в которых располагаются библиотеки для распознавания лиц, прочих форм и дорожных знаков.


## Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков https://dvmn.org/.
