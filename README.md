# ML_in_business

Выполнил: Продан А.Д.

Стек:

ML: sklearn, pandas, numpy API: flask Данные: с kaggle - https://www.kaggle.com/c/realestatepriceprediction

Задача: Предсказать цены на недвижимость
Используемые признаки:

description (text)
DistrictId (number)
Rooms (number)
Square (number)
LifeSquare (number)
KitchenSquare (number)
Floor (number)
HouseFloor (number)
Модель: VotingRegressor (RandomForestRegressor, LGBMRegressor)

Клонируем репозиторий и создаем образ

$ git clone https://github.com/Progul/ML_in_business/tree/master/HW_9

$ cd Machine_/ML_in_Bussines/HW_9

$ docker build -t rush/gb_docker_price_predictions .

Запускаем контейнер

Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180 -v <your_local_path_to_pretrained_models>:/app/app/models rush/gb_docker_price_predictions

Переходим на localhost:8181
