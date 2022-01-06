Итоговый проект по курсу "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy 
API: flask 
Данные: https://www.kaggle.com/c/choose-tutors/data

Задача: предсказать вероятность того, подойдет ли репетитор для подготовки к экзамену по математике (поле choose). Бинарная классификация.

Используемые признаки:

* age, 
* years_of_experience, 
* lesson_price, 
* qualification, 
* physics, 
* chemistry,
* biology, 
* mean_exam_points

Преобразования признаков: создание дополнительных признаков при помощи проведения над некоторыми арифметических операций

Модель: logreg

Клонируем репозиторий и создаем образ
1. git clone https://github.com/kamyninatatyana/Final_project_ML_in_business.git
2. cd Final_project_ML_in_business
3. docker build -t kamyninatatyana/Final_project_ML_in_business .

Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models fimochka/gb_docker_flask_example

Переходим на localhost:8181
