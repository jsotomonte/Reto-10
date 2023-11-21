# Reto-10
## Desarrollar un algoritmo que calcule el promedio de un arreglo de reales
````python
#funcion para el promedio del arreglo
def promedio(arreglo):
    if len(arreglo) == 0:
        return 0 
    suma = sum(arreglo)
    promedio = suma / len(arreglo)
    return promedio

#se pide que ingrese la cantidad de valores en el arreglo
n = int(input("Ingrese la cantidad de números en el arreglo: "))
arreglo = []

#se pide que ingrese numeros n cantidad de veces
for i in range(n):
    numero = float(input(f"Ingrese un número {i + 1}: "))
    arreglo.append(numero)

#muestra el promedio
prom = promedio(arreglo)
print(f"El promedio de los números es: {prom}")
````
## Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño
````python
#funcion de  punto producto
def producto(arreglo1, arreglo2):
    if len(arreglo1) != len(arreglo2):
        True
    
    multi = 0
    for i in range(len(arreglo1)):
        multi += arreglo1[i] * arreglo2[i]
    return multi

#pedir que ingrese los valores de los arreglos
n = int(input("Ingrese la longitud de los arreglos: "))

arreglo1 = []
arreglo2 = []

#se pide que ingrese numeros n cantidad de veces para el primer arreglo 
print("Ingrese los valores del primer arreglo:")
for i in range(n):
    num = float(input(f"Valor {i + 1}: "))
    arreglo1.append(num)

#se pide que ingrese numeros n cantidad de veces para el segundo arreglo 
print("Ingrese los valores del segundo arreglo:")
for i in range(n):
    num = float(input(f"Valor {i + 1}: "))
    arreglo2.append(num)

#se imprime el producto punto 
prod = producto(arreglo1, arreglo2)
print(f"El producto punto de los arreglos es: {prod}")
````
## Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo
````python
def final(arreglo):
    #se usa sorted para que todos las x iguales a 0 vayan al final
    ordenado = sorted(arreglo, key=lambda x: x == 0)
    return ordenado

n = int(input("Ingrese la cantidad de números en el arreglo: "))
arreglo = []


for i in range(n):

    #se pide que ingrese numeros n cantidad de veces
    numero = int(input(f"Ingrese un número {i + 1}: "))
    arreglo.append(numero)
    
#se imprime el resultado
arreglo_final = final(arreglo)
print(arreglo_final)
````
## Revisar que son los algoritmos de sorting, entender bubble-sort (enlace a implementación)
El algoritmo de ordenamiento burbuja es una técnica que se utiliza para organizar elementos en una lista. Su enfoque implica realizar múltiples recorridos a lo largo de la lista, comparando elementos adyacentes y realizando intercambios cuando sea necesario. Durante cada pasada, el objetivo es asegurarse de que el elemento más grande termine en su posición correcta. En otras palabras, cada elemento "burbujea" gradualmente hacia su ubicación final a medida que se realizan comparaciones y intercambios sucesivos. Este proceso se repite hasta que la lista esté completamente ordenada, con los elementos dispuestos de menor a mayor (o viceversa, según el criterio de ordenamiento establecido). El nombre "ordenamiento burbuja" refleja visualmente cómo los elementos más grandes ascienden a través de la lista, similar a burbujas que emergen en una corriente ascendente.
