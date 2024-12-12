# 7-retos-del-reto-5
=========================================================================================================================================================================================

El objetivo era resolver el reto 5, el cual consistia en
realizar algoritmos que cumplieran con las necesidades 
planteadas en cada punto.
A continuacion adjunto la imagen del reto 5 en el repositorio del profe Felipe:

========================================================================================================================================================================================

![image](https://github.com/user-attachments/assets/e227598a-dea3-46ad-8e7e-5d1460e58e7b)

=======================================================================================================================================================================================

>-Asi que adjuntare capturas mostrando como estan
>diseñados los codigos (logica) para cumplir con
>cada punto del reto, los hice todos en un notebook
>de visual studio code para python; igualmente adjunto
>los codigos de cada algoritmo para que puedan ser probados.
>(Cabe aclarar que no se podian usar bucles para simplificar
> los codigos que se mostraran a continuacion, entonces esta
>fue la logica segun el programa del curso)

========================================================================================================================================================================================

![image](https://github.com/user-attachments/assets/86755e9b-b3a6-4701-a18b-ef22eed743f1)

```

import math
def volumen_y_area_superficial_esfera(r:float) -> float:
    volumen_esfera = (4/3)*math.pi*(r**3)
    area_superficial_esfera = 4*math.pi*(r**2)
    return volumen_esfera, area_superficial_esfera
def volumen_y_area_superficial_cono(r2:float,h:float) -> float:
    volumen_cono = (1/3)*math.pi*(r2**2)*h
    area_superficial_cono = math.pi*r2*l+math.pi*(r2**2)
    return volumen_cono, area_superficial_cono
if __name__ == "__main__":
  r = float(input("Ingrese el radio de la esfera:"))
  r2 = float(input("Ingrese el radio de la base del cono:"))
  h = float(input("Ingrese la altura de inclinacion del cono:"))
  volumen, area = volumen_y_area_superficial_esfera(r)
  volumen_2, area_2 = volumen_y_area_superficial_cono(r2,h)
  print(f"El area superficial de la esfera es {area:.2f}" )
  print(f"El volumen de la esfera es {volumen:.2f}" )
  print(f"El area superficial del cono es {area_2:.2f}" )
  print(f"El volumen del cono es {volumen_2:.2f}" )

```

![image](https://github.com/user-attachments/assets/62fc3f5d-4914-47a5-bef7-833af2c570dc)

```

import math
def area_y_perimetro_rectangulo(b:float, a:float) -> float:
    area_rectangulo = a*b
    perimetro_rectangulo = 2*a+2*b
    return area_rectangulo, perimetro_rectangulo
def area_y_perimetro_circulos(r:float) -> float:
    area_circulos = math.pi*(r**2)
    perimetro_circulos = 2*math.pi*r
    return area_circulos, perimetro_circulos
if __name__ == "__main__":
  a = float(input("Ingrese el valor de la altura:"))
  b = float(input("Ingrese el valor de la base:"))
  r = float(input("Ingrese el radio de los circulos:"))
  area, perimetro = area_y_perimetro_rectangulo (b,a)
  area_2, perimetro_2 = area_y_perimetro_circulos (r)
  print(f"El area del rectangulo es {area:.2f}" )
  print(f"El perimetro del rectangulo es {perimetro:.2f}" )
  print(f"El area de los circulos es {area_2:.2f}" )
  print(f"El perimetro de los circulos es {perimetro_2:.2f}" )

```

![image](https://github.com/user-attachments/assets/9ab952e3-2012-4dfd-b3ef-c72843d6459c)

```

def cantidad_carne_en_kilos(n:float, m:float, k:float) -> float:
    cantidad_total = (n*6)+(m*7)+k
    return cantidad_total
if __name__ == "__main__":
  print ("A continucacion debe ingresar la cantidad n de gallinas, la cantidad m de gallos y la cantidad k de pollitos, esto sera necesario para calcular el peso total en kilos de carne")
  print ("(Pues respectivamente las gallinas pesan 6 kilos, los gallos 7 kilos y los pollitos 1 kilo)")
  n = float(input("Ingrese el numero de gallinas:"))
  m = float(input("Ingrese el numero de gallos:"))
  k = float(input("Ingrese el numero de pollitos:"))
  cantidad_total = cantidad_carne_en_kilos (n,m,k)
  print(f"La cantidad total de carne es {cantidad_total:.2f} kilos" )

```

![image](https://github.com/user-attachments/assets/7ebf2aab-ad47-4689-8dd9-04bf0694ced0)

```

def valor_del_prestamo(c:int, i:float, n:int, t:float ) -> int:
    valor_final = c*(1+i/n)**(n*t)
    return valor_final
if __name__ == "__main__":
    c = int(input("Ingrese la cantidad del prestamo:"))
    i = float(input("Ingrese la tasa de interes:"))
    n = int(input("Ingrese el numero de veces que se aplica el interes por periodo:"))
    t = float(input("Ingrese el numero de periodos transcurridos:"))
    valor_final = valor_del_prestamo (c, i, n, t)
    print (f"el valor final del prestamo que debe pagar es: {int(valor_final)} pesos")

```

![image](https://github.com/user-attachments/assets/3d62432d-0153-4baf-a116-fce3bcf78f28)

```

def promedio(a:float, b:float, c:float, d:float, e:float) -> float:
    resultado = (a+b+c+d+e)/5
    return resultado
def promedio_multiplicativo(a:float, b:float, c:float, d:float, e:float) -> float:
    resultado_2 = (a*b*c*d*e)**(1/5)
    return resultado_2
def potencia(a:float, b:float, c:float, d:float, e:float) -> float:
    if a > b and a > c and a > d and a > e: 
        mayor = a
    elif b > a and b > c and b > d and b > e: 
        mayor = b
    elif c > a and c > b and c > d and c > e:
        mayor = c
    elif d > a and d > b and d > c and d > e:
        mayor = d
    else:
        mayor = e
    if a < b and a < c and a < d and a < e:
        menor = a
    elif b < a and b < c and b < d and b < e:
        menor = b
    elif c < a and c < b and c < d and c < e:
        menor = c
    elif d < a and d < b and d < c and d < e:
        menor = d
    else:
        menor = e
    resultado_3 = mayor ** menor, mayor, menor
    return resultado_3
def raiz_cubica(a:float, b:float, c:float, d:float, e:float) -> float:
    if a < b and a < c and a < d and a < e:
        menor_2 = a
    elif b < a and b < c and b < d and b < e:
        menor_2 = b
    elif c < a and c < b and c < d and c < e:
        menor_2 = c
    elif d < a and d < b and d < c and d < e:
        menor_2 = d
    else:
        menor_2 = e
    resultado_4 = menor_2 ** (1/3)
    return resultado_4, menor_2
if __name__ == "__main__":
  a = float(input("Ingrese el primer número real:"))
  b = float(input("Ingrese el segundo número real:"))
  c = float(input("Ingrese el tercer número real:"))
  d = float(input("Ingrese el cuarto número real:"))
  e = float(input("Ingrese el quinto número real:"))
  resultado = promedio (a,b,c,d,e)
  resultado_2 = promedio_multiplicativo (a,b,c,d,e)
  resultado_3, mayor, menor = potencia (a,b,c,d,e)
  resultado_4, menor_2 = raiz_cubica (a,b,c,d,e)
print(f"El promedio de los 5 números es: {resultado:.2f}")
print(f"El promedio multiplicativo de los 5 números es: {resultado_2:.2f}")
print(f"La potencia de el mayor numero ({mayor}) elevado al menor numero ({menor}) es: {resultado_3:.2f}")
print(f"La raíz cúbica del menor número ({menor_2}) es: {resultado_4:.2f}")

```

>-PD : PERDON POR NO ACTIVAR WINDOWS JAJA

========================================================================================================================================================================================

>-PUNTO 6 Y 7

========================================================================================================================================================================================
## QUE ES PIP Y COMO FUNCIONA EN PYTHON

-_Pip_ es un sistema de gestion de paquetes usado para instalar y administrar paquetes de software escritos en python con fin de descargarlos en nuestra computadora para utilizarlos en nuestros algoritmos desarrollados en python

>- Muchos paquetes pueden ser encontrados en el Python Package Index (PyPI).
>- Python 3.4 y posteriores incluyen pip (pip3 para Python3) por defecto; lo
>cual no es necesario instalarlo en nuestra pc ya que al instalar python en la
>version 3.4 o superior en automaático se instala el gestor de paquetes.

-Una de las principales ventajas de utilizar el gestor de paquetes Python es el número de librerías o bibliotecas de código excelentes que están amplia y fácilmente disponibles y que te pueden ahorrar escribir mucho código, o simplemente realizar una tarea particular de la manera más sencilla.

## COMO INSTALAR PIP PARA PYTHHON EN WINDOWS

![image](https://github.com/user-attachments/assets/a5af884e-f110-4c7f-8e6a-d73ec13c1ce0)

## QUE ES UNA LIBRERIA EN PYTHON

-A grandes rasgos, cabe destacar que en programación una librería responde al conjunto de funcionalidades que permiten al usuario  llevar a cabo nuevas tareas que antes no se podían realizar.

-Es decir, las librerías de Python responden al conjunto de implementaciones que permiten codificar este lenguaje, con el objeto de crear una interfaz independiente.

## COMO INSTALAR LIBRERIAS EN PYTHON

![image](https://github.com/user-attachments/assets/5867a6e7-9a6b-4270-bce7-7c962538ec1b)

========================================================================================================================================================================================
## CUALES SON LAS LIBRERIAS MAS POPULARES DE PYTHON

-Segun el Inmune Technology Institute (Centro de formación ubicado en Madrid, España) estas son las mejores 9 librerias para usar en python 

![image](https://github.com/user-attachments/assets/1894791e-3ef0-4f30-ae7c-6b4b5bb2ec7f)
![image](https://github.com/user-attachments/assets/4fb52870-cf9f-4897-8425-2719863c1068)

========================================================================================================================================================================================

# BIBLIOGRAFIAS

La informacion presentada en este repositorio fue toma de:
-[buscaminegocio]: <(https://www.buscaminegocio.com/cursos-de-python/pip-en-python.html)>
-[inmune.institute]: <(https://immune.institute/blog/librerias-python-que-son/)>
-[tecnonucleous]: <(https://tecnonucleous.com/2018/01/28/como-instalar-pip-para-python-en-windows-mac-y-linux/)>

========================================================================================================================================================================================

# NICOLAS RAMIREZ RODRIGUEZ 1000506513
