# Actividad Paint
## Autor:
*Angel Alejandro Rosas Díaz A01411376*
## Funciones agregadas:
*Se implementaron los datos del autor*
## Codigo:
def info_alumnos():
    writer.up()
    writer.goto(-30,190)
    writer.color("blue")
    writer.write("Angel Alejandro Rosas Diaz A01411376", align = "left", font = ("Arial", 10, "normal"))
  
## Funciones agregadas:
*El cursor genera 4 lineas iguales, las cuales haran un giro de 90 grados de esta manera para crear un cuadrado y se uso la funcion fill para rellenarlo*
## Codigo:
def square(start, end):
    "Draw square from start to end."
    up()
    goto(start.x, start.y)
    down()
    begin_fill()
    for count in range(4):
        forward(end.x - start.x)
        right(90)
    end_fill()
    
 ## Funciones Agregadas: 
 *Se utilizo la libreria math para insertar una raiz cuadrada y esta nos permitio tener la formula de radio del circulo para que el programa pudiera generar automaticamente esta figura*
 ## Codigo:
 def circ(start, end):
    "Draw circle from start to end."
    rad = math.sqrt((end.x - start.x)*2 + (end.y - start.y)*2)
    center = start.y - rad
    up()
    goto(start.x, center)
    down()
    begin_fill()
    circle(rad)
    end_fill()
    
 ## Funciones agregadas:
 *Se repite 2 veces el ciclo para hacer una linea girar 90 grados, despues una linea a la mitad del tamaño de esta gira 90 grados y al finalizar la figura se rellena*
 ## Codigo:
 def rectangle(start, end):
    "Draw rectangle from start to end."
    up()
    goto(start.x, start.y)
    down()
    begin_fill()
    for count in range(2):
        forward(end.x - start.x)
        left(90)
        forward((end.x - start.x) / 2)
        left(90)
    end_fill()
    
 ## Funciones agregadas:
 *Se imprime una linea 3 veces con angulos de 120 grados para generar un triangulo equilatero*
 ## Codigo:
 def triangle(start, end):
    "Draw triangle from start to end."
    up()
    goto(start.x, start.y)
    down()
    begin_fill()
    for count in range(3):
        forward(end.x - start.x)
        left(120)
    end_fill()
    
 ## Funciones agregadas:
 *Al final del codigo se utiliza esta funcion para que la librería Turtle se guardara como .writer para poder utilizarse en info_alumnos() y clear para que se pueda borrar facilmente el paint y no tener que reiniciarlo o picarle al undo muchas veces*
## Codigo:
writer = Turtle(visible = False)
info_alumnos()

onkey(clear, 'C')
