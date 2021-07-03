# python-flask-docker
Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy
API: flask
Данные: с kaggle - https://archive.ics.uci.edu/ml/machine-learning-databases/00591/name_gender_dataset.csv

Задача: предсказать по имени пол человека. Бинарная классификация

Используемые признаки:

- name (text)

Преобразования признаков: get_dummies

Модель: CatBoostClassifier

### Клонируем репозиторий и создаем образ
```
$ git clone https://github.com/amerus/name_to_gender.git
$ cd name_to_gender
$ docker build -t amerus/name_to_gender .
```

### Запускаем контейнер

Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель и columns.csv файл с названиями признаков (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)
```
$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models amerus/name_to_gender
```

### Переходим на localhost:8181
