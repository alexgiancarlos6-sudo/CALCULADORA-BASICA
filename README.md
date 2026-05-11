# CALCULADORA-BASICA
Una calculadora simple y basica 
Aquí tienes un código de Python para una calculadora básica. Este programa permite al usuario realizar sumas, restas, multiplicaciones y divisiones, e incluye manejo de errores básicos (como evitar que el programa falle si intentas dividir por cero o si ingresas letras en lugar de números).

Código de la Calculadora en Python
Python
def sumar(x, y):
    return x + y

def restar(x, y):
    return x - y

def multiplicar(x, y):
    return x * y

def dividir(x, y):
    if y == 0:
        return "Error: No se puede dividir por cero."
    return x / y

def calculadora():
    print("--- Calculadora Básica ---")
    print("Selecciona la operación:")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")

    while True:
        # Pedimos al usuario que elija una opción
        opcion = input("\nIngresa el número de la operación (1/2/3/4) o 'q' para salir: ")

        # Condición para salir del bucle
        if opcion.lower() == 'q':
            print("¡Hasta luego!")
            break

        # Verificamos si la opción es válida
        if opcion in ('1', '2', '3', '4'):
            try:
                # Pedimos los números y los convertimos a decimales (float)
                num1 = float(input("Ingresa el primer número: "))
                num2 = float(input("Ingresa el segundo número: "))
            except ValueError:
                print("Entrada no válida. Por favor, ingresa solo números.")
                continue

            # Realizamos la operación correspondiente
            if opcion == '1':
                print(f"Resultado: {num1} + {num2} = {sumar(num1, num2)}")
            elif opcion == '2':
                print(f"Resultado: {num1} - {num2} = {restar(num1, num2)}")
            elif opcion == '3':
                print(f"Resultado: {num1} * {num2} = {multiplicar(num1, num2)}")
            elif opcion == '4':
                print(f"Resultado: {num1} / {num2} = {dividir(num1, num2)}")
        else:
            print("Opción no válida. Por favor, selecciona 1, 2, 3 o 4.")
            2+2
            
