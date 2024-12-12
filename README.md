# Cuarto Dia Pa Roma
En este repositorio desarrollaremos una serie de ejercicios en los cuales ponemos en práctica el uso de funciones en Python
### Ejercicio 1
Conociendo el radio de una esfera y, el radio de un cono con su altura determine el área y volumen total de ambas piezas.
```python
import math
def volumen_total(r1: float, r2: float, h: float) -> float:
  volumen_esfera = 4/3 * math.pi * r1**3
  volumen_cono = 1/3 * math.pi * (r2**2) * h
  return volumen_esfera + volumen_cono

def area_total(r1: float, r2: float, h: float) -> float:
  area_esfera = 4 * math.pi * r1**2
  area_cono = r2**2 * math.pi + math.pi * r2 * (r2**2 + h**2)**0.5
  return area_esfera + area_cono

if __name__ == "__main__":
  r1 = float(input("Ingrese el radio de la esfera: "))
  r2 = float(input("Ingrese el radio del cono: "))
  h = float(input("Ingrese la altura del cono: "))
  volumen = volumen_total(r1, r2, h)
  print("El volumen total de los objetos es " + str(volumen))
  area = area_total(r1, r2, h)
  print("El área total de los objetos es " + str(area))
```
### Ejercicio 2
Conociendo los lados de un rectángulo y el radio que comparten dos círculos determine: el área y el pérímetro total de las figuras.
```python
import math

def perimetro(a: float, b: float, r: float) -> float:
    perimetro_rec = 2 * a + 2 * b
    perimetro_cir = 2 * r * math.pi * 2 #El 2 al final es porque son 2 circunferencias.
    return perimetro_rec + perimetro_cir

def area(a: float, b: float, r: float) -> float:
    area_rec = a * b
    area_cir = r**2 * math.pi * 2 #El 2 al final es porque son 2 círculos.
    return area_rec + area_cir

if __name__ == "__main__":
  a = float(input("Ingrese la logitud del lado a: "))
  b = float(input("Ingrese la logitud del lado b: "))
  r = float(input("Ingrese la logitud del radio: "))
  perimetro_total = perimetro(a, b, r)
  print(perimetro_total)
  area_total = area(a, b, r)
  print(area_total)
```
### Ejercicio 3
Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.
```python
def peso_aves(n: float, m: float, k: float) -> float:
  peso_n = n * 6
  peso_m = m * 7
  peso_k = k
  return peso_n + peso_m + peso_k

if __name__ == "__main__":
  n = (float(input("Cantidad de Gallinas(kg): ")))
  m = (float(input("Cantidad de Gallos(kg): ")))
  k = (float(input("Cantidad de Pollitos(kg): ")))
  peso_total = peso_aves(n, m, k)
  print("La cantadidad total de carne es de " + str(peso_total) + "kg")
```
### Ejercicio 4
Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
```python
def interes_compuesto(c: float, i: float, n: float) -> float:
  interes = c*(1+i)**n
  return interes

if __name__ == "__main__":
  c = (float(input("Ingrese capital inicial: ")))
  i = (float(input("Ingrese el tipo de interés: ")))
  n = (float(input("Ingrese el tiempo(años): ")))
  monto_final = interes_compuesto(c, n, i)
  print("El capital final es de: " + str(monto_final))
```
### Ejercicio 5
Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

* El promedio
* El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
* La potencia del mayor número elevado al menor número
* La raíz cúbica del menor número
```python
def promedio(a: float, b: float, c: float, d: float, e: float) -> float:
  prom = (a+b+c+d+e)/5
  return prom

def promedio_multiplicativo(a: float, b: float, c: float, d: float, e: float) -> float:
  prom_mul = (a*b*c*d*e)**(1/5)
  return prom_mul

def potencia_mayor_menor(a: float, b: float, c: float, d: float, e: float) -> float:
  num_max = max(a, b, c, d, e) #max es para encontrar el valor máximo de una lista de números
  num_min = min(a, b, c, d, e) #min es para encontrar el valor mínimo de una lista de números
  potencia = num_max**num_min
  return potencia

def raiz_cub_menor(a: float, b: float, c: float, d: float, e: float) -> float:
  num_min = min(a, b, c, d, e)
  raiz_cubica = num_min**(1/3)
  return raiz_cubica

if __name__ == "__main__":
  a = (float(input("Ingrese el primer número: ")))
  b = (float(input("Ingrese el segundo número: ")))
  c = (float(input("Ingrese el tercer número: ")))
  d = (float(input("Ingrese el cuarto número: ")))
  e = (float(input("Ingrese el quinto número: ")))
  prom = promedio(a, b, c, d, e)
  print("El promedio es: " + str(prom))
  prom_mul = promedio_multiplicativo(a, b, c, d, e)
  print("El promedio multiplicativo es: " + str(prom_mul))
  potencia = potencia_mayor_menor(a, b, c, d, e)
  print("La potencia del mayor número elevado al menor número es: " + str(potencia))
  raiz_cub = raiz_cub_menor(a, b, c, d, e)

  print("La raíz cúbica del menor número es: " + str(raiz_cub))
```
