# RAIFHACK
Идея следующая:
1) Обучить модель используя автомл на датасете, который более валидный - т.е. данные, у которых price_type = 1.
2) Предсказать цену для всего датасета, включая тестовый. (скор на тестовом ~ 1.57)
3) Затем отобрать из датасета с price_type = 0 те значения, которые не сильно отличаются от предсказанного. Я испоользовал порог 10%, можно попробовать другие. Идея в том, чтобы не брать в тренировочный датасет данные с выбросами. (Если посомтреть медиану, то на датасете с price_type = 1 она меньше на 20%) 
4) Предсказать итоговый скор на полученном датасете с новой фичей. Скор получился ~1.53. Получался даже 1.5, но параметры, к сожалению, не сохранились:(
