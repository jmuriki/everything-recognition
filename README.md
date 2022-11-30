# everything-recognition

Данный проект в режиме реального времени выводит видео с веб-камеры, на котором распознаёт человеческие лица и прочие объекты, подсвечивая их цветными прямоугольными рамками.


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

Скрипт подключается к веб-камере, распознаёт в полученном видео-потоке различные объекты, а затем выводит видео на экран, обозначая на нём распознанные объекты цветными рамками.

Если не удастся обнаружить веб-камеру, скрипт выведет соответствующее сообщение.


### config.py

Здесь содержатся настройки и пути к библиотекам для распознавания объектов. Можно включать/выключать распознавание и выделение на видео лиц, профилей, улыбок, глаз, тел и кошачьих мордочек, а также задавать цвет выделения.

Для изменения настроек, поэкспериментируйте с `"path"`, `"color"` и `"draw"`.

По аналогии можно подключить любые библиотеки, находящиеся в папке `haarcascades`, указав к ним путь, выбрав цвет рамок и поставив значение `"draw": True`.


### haarcascades

В этой директории находятся библиотеки `banana_classifier.xml` и `cars.xml`, а также папки `road-signs` и `faces`, в которых располагаются библиотеки для распознавания дорожных знаков, лиц и прочих форм.


## Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков https://dvmn.org/.
