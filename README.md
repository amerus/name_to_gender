# python-flask-docker
Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy<br>
API: flask<br>
Данные: https://archive.ics.uci.edu/ml/machine-learning-databases/00591/name_gender_dataset.csv

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

```
$ ./vanilla.sh
```

### Альтернативный подход
```
Вместо локального docker build, можно скачать готовый образ из репозитория на Docker Hub:<br> 
$ docker pull amerus/name_to_gender 


### Переходим на localhost:8181 или работаем с Jupyter Notebook FinalProject.ipynb
