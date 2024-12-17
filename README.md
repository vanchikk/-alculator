# -alculator
Simple calculator with a loop

while True:
    try:
        num1 = float(input("Введіть перше число: "))

        operation = input("Введіть операцію (+, -, *, /): ")

        num2 = float(input("Введіть друге число: "))

        if operation == '+':
            result = num1 + num2
        elif operation == '-':
            result = num1 - num2
        elif operation == '*':
            result = num1 * num2
        elif operation == '/':
            if num2 == 0:
                print("Помилка: Ділення на нуль неможливе!")
                continue
            result = num1 / num2
        else:
            print("Невірна операція!")
            continue

        print(f"Результат: {result}")

    except ValueError:
        print("Помилка: Ви ввели некоректне число!")
        continue
    
    choice = input("Бажаєте продовжити? (y/yes для продовження): ").lower()
    if choice not in ['y', 'yes']:
        print("Калькулятор завершив роботу.")
        break
