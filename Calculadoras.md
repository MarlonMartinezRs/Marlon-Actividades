# Marlon-Actividades
Actividades Realizadas en clase
--CALCULADORA DE INTERÉS COMPUESTO--

principal = float(input("Ingrese la cantidad principal: "))
tasa_interes = float(input("Ingrese la tasa de interés (porcentaje): "))
tiempo = int(input("Ingrese el tiempo en años: "))

tasa_interes /= 100  # Convertir la tasa de interés a decimal
monto_final = principal * (1 + tasa_interes) ** tiempo
print(f"El monto final es: {monto_final:.2f}")

--GENERADOR DE CONTRASEÑAS--

import random
import string

longitud = int(input("Ingrese la longitud de la contraseña: "))

caracteres = string.ascii_letters + string.digits + string.punctuation
contrasena = ''.join(random.choice(caracteres) for _ in range(longitud))

print(f"Contraseña generada: {contrasena}")

--VERIFICAR SI EL NUMERO ES PRIMO--

numero = int(input("Ingrese un número: "))
es_primo = True
if numero <= 1:
    es_primo = False
else:
    for i in range(2, int(numero**0.5) + 1):
        if numero % i == 0:
            es_primo = False
            break
if es_primo:
    print(f"{numero} es un número primo.")
else:
    print(f"{numero} no es un número primo.")

    --TABLA DE MULTITPLICAR--

    numero = int(input("Ingrese un número para mostrar su tabla de multiplicar: "))
for i in range(1, 11):
    resultado = numero * i
    print(f"{numero} x {i} = {resultado}")
