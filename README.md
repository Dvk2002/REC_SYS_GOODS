Рекомендательная система создана на основе двухуровневой модели.
На первом этапе кандидаты отбираются на основе собственных покупок юзера (ItemItemRecommender),
на основе предсказаний модели AlternatingLeastSquares и топ покупок самого юзера.
На втором этапе данные подготовливаются для модели классификации, и затем используется ансамбль
из Catboost и LGBM.
Подбор гиперпараметров и оценка новых признаков происходила на валидационном сете, 
итоговое предсказание - на тестовом.
Метрика качества - precision_at_5.
