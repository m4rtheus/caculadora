while True:
    number_1 = input("Digite um número: ")
    number_2 = input("Digite outro número: ")
    oparator = input("Digite um operador (+-/*): ")

    valid_number = True
    number_1_float = 0
    number_2_float = 0

    try:
        number_1_float = float(number_1)
        number_2_float = float(number_2)
        valid_number = True

    except:
        valid_number = None

    if valid_number is None:
        print("Um ou ambos os números são invalidos.")
        continue

    valid_oparator = "+-/*"

    if oparator not in valid_oparator:
        print("operador invalido.")
        continue

    if len(oparator) > 1:
        print("Escolha apenas um operador.")
        continue

    print("Estamos realizando a operação, veja o resultado abaixo: ")

    if oparator == "+":
        print(number_1_float + number_2_float)

    elif oparator == "-":
        print(number_1_float - number_2_float)

    elif oparator == "/":
        if number_2_float == 0:
            print("Não é possível dividir um valor por zero.")
        else:
            print(number_1_float / number_2_float)
    
    elif oparator == "*":
         print(number_1_float * number_2_float)

    else:
        print("Você nunca devia ter chegado até aqui.")

    sair = input("Você quer [s]air? ").lower().startswith("s")

    if sair is True:
        break
