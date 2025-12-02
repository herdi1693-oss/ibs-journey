print("ИНдекс массы тела")

def vod_dannyh_recursive(prompt, min_value, max_value, attempt=1, max_attempts=3):
    """
    Рекурсивная версия ввода с валидацией.
    
    Args:
        prompt (str): Текст запроса
        min_value (float): Минимальное значение
        max_value (float): Максимальное значение
        attempt (int): Текущая попытка (начинается с 1)
        max_attempts (int): Максимальное количество попыток
    
    Returns:
        float: Проверенное число
    
    Raises:
        ValueError: Если превышено количество попыток
    """
    # Базовый случай: превышено количество попыток
    if attempt > max_attempts:
        raise ValueError(f"Превышено количество попыток ({max_attempts})")
    
    try:
        # Запрашиваем ввод
        user_input = input(f"{prompt} (попытка {attempt}/{max_attempts}): ")
        value = float(user_input.replace(',', '.'))
        
        # Проверяем диапазон
        if min_value <= value <= max_value:
            return value
        else:
            print(f"Ошибка: число должно быть между {min_value} и {max_value}")
            # Рекурсивный вызов для следующей попытки
            return vod_dannyh_recursive(prompt, min_value, max_value, attempt + 1, max_attempts)
    
    except ValueError:
        print(f"Ошибка: '{user_input}' не является числом")
        # Рекурсивный вызов для следующей попытки
        return vod_dannyh_recursive(prompt, min_value, max_value, attempt + 1, max_attempts)

#def vod_dannyh(promt, min_value, max_value):
#    while True:
#        promt_input = input("Введите число ")
#        try:
#            promt = float(promt_input.replace(',', '.'))
#            if min_value <= promt <= max_value:
#                return promt
#            else:
#                print("Ошибка диапазона")
#        except ValueError:
#            print("Ошибка формата")
print("Ведите вес ")    
ves = vod_dannyh_recursive("Ведите вес", 10, 300)
print("Ведите рост ")  
rost = vod_dannyh_recursive("Ведите рост", 0.5, 2.5)
#ves_input = input("введите вес: ")
#while True:
#    try:
#        ves = float(ves_input.replace(',', '.'))
#        break
#    except:
#        ves_input = input("ведите число ")
#rost_input = input("введите рост в метрах: ")
#while True:
#    try:
#        rost = float(rost_input.replace(',', '.'))
#        if rost != 0:
#            break
#        else:
#            rost_input = input("ведите число не равное 0 ")
#    except:
#        rost_input = input("ведите число ")
imt = round(ves / (rost * rost), 2)
if imt < 18.5:
    print (f"недобор веса, ИМТ = {imt} ")
elif 18.5 <= imt <25:
    print(f"нормальный вес, ИМТ = {imt}  ")
elif 25 <= imt < 30:
    print(f"избыточный вес, ИМТ = {imt}  ")
else:
    print(f"ну ты и свинья, ИМТ = {imt}  ")
