# Examen Tipo Test – Estructuras de Datos I

## Preguntas


1. **¿Qué ocurre al ejecutar el siguiente código?**

```cpp
float *tabla = new float[3]; 
tabla[0] = 1.0; tabla[1] = 2.0; tabla[2] = 3.0;
cout << *(tabla + 3);
```
A) Se imprime 0.0
B) Error de compilación
C) Acceso a memoria inválida (comportamiento indefinido)
D) Se imprime 3.0

2. **¿Qué error contiene el siguiente código para insertar al principio de una lista?**

```cpp
void insertarInicio(TNodo_Lista *lista, float dato) {
    TNodo_Lista *nuevo = new TNodo_Lista;
    nuevo->Datos = dato;
    nuevo->Siguiente = lista;
    lista = nuevo;
}
```
A) No se reserva memoria correctamente
B) No se actualiza el puntero original
C) El puntero Siguiente queda sin inicializar
D) El valor dato no se almacena

3. **¿Qué imprime este código?**

```cpp
int valor = 10;
int *p = &valor;
*p = *p + 5;
cout << valor;
```
A) 5
B) 10
C) 15
D) Error de compilación

4. **Dado el siguiente fragmento:**

```cpp
ifstream fichero("datos.bin", ios::binary);
fichero.seekg(0, ios::end);
int tam = fichero.tellg();
```
¿Cuál es el objetivo de este código?

A) Mover el puntero de escritura al final
B) Leer el último byte del fichero
C) Obtener el tamaño del fichero en bytes
D) Vaciar el fichero antes de lectura

5. **¿Qué problema presenta esta función?**

```cpp
void borrarLista(TNodo_Lista* lista) {
    while (lista != NULL) {
        TNodo_Lista* tmp = lista->Siguiente;
        delete lista;
        lista = tmp;
    }
}
```
A) Puede liberar nodos no inicializados
B) No borra todos los nodos
C) El puntero externo sigue apuntando a memoria liberada
D) No libera correctamente la memoria

6. **¿Qué hace esta plantilla?**

```cpp
template <class T>
T mayor(T a, T b) {
    return (a < b) ? b : a;
}
```
A) Calcula el menor entre a y b
B) Siempre retorna a
C) Retorna el mayor entre a y b
D) Compara cadenas por longitud

7. **¿Cuál es el efecto del siguiente código?**

```cpp
ifstream entrada("datos", ios::binary);
entrada.read((char*)&x, sizeof(int));
```
A) Lee un carácter desde el fichero
B) Lee un entero desde el fichero
C) Guarda una cadena de texto
D) Escribe un entero en el fichero

8. **¿Qué ocurre si se usa delete[] sobre un puntero que fue creado con new (sin corchetes)?**

A) Libera correctamente la memoria
B) Provoca comportamiento indefinido
C) No tiene efecto
D) El compilador da un error

9. **¿Cuál es la diferencia entre seekg y seekp en C++?**

A) seekg posiciona para escritura, seekp para lectura
B) Ambas posicionan para lectura
C) seekg es para lectura, seekp para escritura
D) No hay diferencia

10. **¿Cuál es el resultado del siguiente código?**

```cpp
template <class T>
T suma(T a, T b) {
    return a + b;
}

cout << suma<string>("Hola ", "mundo");
```
A) Error de compilación
B) "Hola mundo"
C) "Holamundo" sin espacio
D) "mundohola"

11. **¿Cuál de estas estructuras es más eficiente en inserciones al principio de una lista?**

A) Vector estático
B) Lista doblemente enlazada
C) Lista simplemente enlazada
D) Array dinámico

12. **Entre estas alternativas, ¿cuál es mejor para una pila de gran volumen donde se apilan y desapilan elementos constantemente?**

A) Lista doblemente enlazada
B) Array de tamaño fijo
C) Array dinámico con redimensionamiento
D) Lista simplemente enlazada

13. **¿Cuál es el mayor inconveniente de las tablas dinámicas frente a listas enlazadas?**

A) El acceso aleatorio
B) El uso de punteros
C) La sobrecarga en inserciones intermedias
D) La necesidad de redimensionamiento

14. **¿Qué factor hace que las colas implementadas con listas sean preferibles a vectores circulares en algunos contextos?**

A) Menor coste de memoria
B) Mayor eficiencia de acceso
C) Ausencia de límite predefinido
D) Uso de funciones recursivas

15. **¿Qué es un TAD?**

A) Un tipo de datos específico de C++
B) Una estructura física de datos
C) Un tipo de datos definido con especificación abstracta e independiente de implementación
D) Una función genérica

16. **¿Qué define una especificación algebraica?**

A) Una función sobre tipos primitivos
B) La representación en memoria del TAD
C) Un conjunto de operaciones y ecuaciones formales sobre los tipos
D) Un compilador optimizado

17. **Dado el siguiente código:**

```cpp
TLista<float> lista;
lista.insertar(1, 5.5);
lista.eliminar(1);
cout << lista.esvacia();
```
¿Qué imprime?

A) 0
B) 1
C) true
D) Error de compilación

18. **¿Qué implica declarar template <class T> antes de una clase?**

A) Que la clase solo trabaja con enteros
B) Que la clase puede aceptar diferentes tipos de datos
C) Que no se puede usar herencia
D) Que los métodos no pueden ser definidos fuera de la clase

19. **¿Qué sucede si no se define el destructor en una clase con memoria dinámica?**

A) Se libera la memoria automáticamente
B) Se produce un error de compilación
C) Puede haber fuga de memoria
D) No se puede instanciar la clase

20. **¿Qué operador permite acceder a los campos de una estructura apuntada por puntero?**

A) .
B) ->
C) *
D) &


21. **¿Cuál es el resultado de ejecutar este código?**

```cpp
float *p = NULL;
if (!p) cout << "Puntero nulo";
```
A) Error de compilación
B) No imprime nada
C) Imprime "Puntero nulo"
D) Depende del sistema operativo

22. **¿Qué hace este código?**

```cpp
int v[] = {1, 2, 3};
cout << *(v + 1);
```
A) Error de compilación
B) Imprime 1
C) Imprime 2
D) Imprime la dirección de memoria

23. **¿Qué tipo de acceso permite esta operación?**

```cpp
fichero.seekg(3 * sizeof(ficha), ios::beg);
```
A) Secuencial
B) Directo aleatorio
C) Circular
D) Binario secuencial

24. **¿Qué error puede causar el siguiente código?**

```cpp
TLista<float> lista;
lista.insertar(10, 2.5);
```
A) Insertar al final de la lista
B) Insertar fuera de rango
C) Redimensionamiento automático
D) Error por tipo de datos

25. **¿Cuál es el propósito del método clear() en el manejo de ficheros en C++?**

A) Vaciar el contenido del archivo
B) Borrar errores de estado del flujo
C) Eliminar el fichero del sistema
D) Cerrar el archivo automáticamente

26. **Dado este código, ¿qué salida produce?**

```cpp
template <class T>
T multiplicar(T a, T b) {
    return a * b;
}
cout << multiplicar(3, 4);
```
A) 12
B) 7
C) Error de compilación
D) 1

27. **¿Qué sucede si no se cierra un archivo con close()?**

A) El contenido no se guarda correctamente
B) El archivo se borra
C) Se genera una excepción
D) Nada; se cierra automáticamente

28. **¿Qué operador se usa para obtener la dirección de una variable?**

A) *
B) ->
C) &
D) %

29. **¿Qué error se encuentra en este código?**

```cpp
TLista<float> lista;
lista.modificar(3, 4.5);
```
A) No se puede modificar un elemento sin insertarlo antes
B) El tipo float no es compatible
C) modificar no está permitido en listas genéricas
D) El índice 3 es inválido en una lista vacía

30. **¿Qué ocurre al aplicar delete sobre un puntero que ya fue liberado?**

A) Se vuelve a liberar correctamente
B) Se libera la memoria duplicada
C) Comportamiento indefinido
D) El compilador ignora la instrucción

31. **¿Qué implementación es más eficiente en cuanto a uso de memoria?**

A) Lista simplemente enlazada
B) Lista doblemente enlazada
C) Tabla dinámica
D) Lista estática

32. **¿Por qué usar punteros a punteros en listas?**

A) Para obtener más memoria
B) Para modificar la dirección del puntero original
C) Para evitar errores de compilación
D) Para crear nodos en memoria estática

33. **En una pila implementada con nodo enlazado, ¿qué ventaja clave existe?**

A) Acceso aleatorio rápido
B) Menor uso de punteros
C) Inserción/eliminación en O(1)
D) Capacidad limitada

34. **¿Qué ventaja presentan las plantillas de clases?**

A) Menor velocidad de ejecución
B) Menor uso de punteros
C) Reutilización de código con tipos distintos
D) Restricción de uso a un solo tipo

35. **¿Qué es una plantilla de función en C++?**

A) Una función con parámetros constantes
B) Una forma de definir funciones genéricas
C) Una función que siempre devuelve un entero
D) Una macro preprocesada

36. **¿Qué representa una operación observadora en un TAD?**

A) Una operación que modifica datos
B) Una operación que crea estructuras
C) Una operación que consulta información sin modificarla
D) Una operación no definida

37. **¿Qué hace el operador ->?**

A) Declara una clase
B) Declara una función
C) Accede a un miembro desde un puntero a objeto
D) Comparación entre objetos

38. **¿Qué hace este código?**

```cpp
ifstream f("datos", ios::binary);
f.read((char*)&x, sizeof(x));
```
A) Escribe un entero en el archivo
B) Lee bytes del archivo a la variable x
C) Cierra el archivo
D) Imprime el contenido de x

39. **¿Qué significa que una plantilla esté sobrecargada?**

A) Que no funciona correctamente
B) Que tiene demasiados tipos
C) Que existen varias definiciones con mismo nombre y diferente signatura
D) Que solo se aplica a un tipo

40. **¿Para qué sirve template <class T> antes de una función?**

A) Para evitar errores de compilación
B) Para crear funciones independientes del tipo
C) Para definir macros
D) Para definir funciones recursivas


41. **¿Qué sucede si usamos delete[] sobre un puntero que no fue inicializado con new[]?**

A) Se libera correctamente
B) Se ignora la instrucción
C) Provoca comportamiento indefinido
D) Se lanza una excepción

42. **¿Qué imprime este código?**

```cpp
int v[] = {10, 20, 30};
int *p = v;
cout << *(p + 2);
```
A) 10
B) 20
C) 30
D) Error de compilación

43. **¿Qué ventaja ofrece una cola implementada con nodos frente a una con vector circular?**

A) Más eficiencia en el acceso
B) Menor uso de memoria
C) No tiene límite de capacidad predefinido
D) Mayor velocidad de escritura

44. **¿Cuál es el objetivo de esta plantilla?**

```cpp
template <typename T>
T menor(T a, T b) {
    return (a < b) ? a : b;
}
```
A) Retornar siempre b
B) Retornar el mayor
C) Retornar el menor
D) Intercambiar a y b

45. **¿Cuál es el propósito del operador * cuando se usa con punteros?**

A) Multiplicación
B) Declarar punteros
C) Acceso al contenido apuntado
D) Comparación entre punteros

46. **¿Cuál es el efecto de no implementar un constructor de copia en una clase que usa memoria dinámica?**

A) Mejora el rendimiento
B) Permite compartir memoria sin riesgos
C) Provoca errores de doble liberación o fugas de memoria
D) No tiene consecuencias

47. **¿Cuál es la salida de este código?**

```cpp
TLista<int> l;
l.insertar(1, 7);
cout << l.observar(1);
```
A) Error de compilación
B) 0
C) 7
D) -1

48. **¿Qué ocurre si se llama a desencolar() en una cola vacía?**

A) Inserta un elemento nulo
B) Borra toda la memoria
C) Produce comportamiento indefinido si no se comprueba antes
D) No tiene efecto

49. **¿Qué hace este fragmento?**

```cpp
ifstream entrada("fichero.bin", ios::binary);
entrada.seekg(0, ios::end);
long tam = entrada.tellg();
```
A) Mueve el puntero al inicio del archivo
B) Calcula el tamaño del archivo en bytes
C) Muestra los datos del archivo
D) Abre el archivo en modo de texto

50. **¿Qué imprime este código?**

```cpp
float f = 3.5, *pf = &f;
cout << *pf;
```
A) Dirección de memoria
B) Error de compilación
C) 3.5
D) NULL

51. **¿Por qué usar una lista doblemente enlazada en lugar de una simple?**

A) Menor complejidad de código
B) Mayor eficiencia en acceso aleatorio
C) Permite recorrer en ambos sentidos
D) Requiere menos memoria

52. **¿Qué ventaja tiene el uso de plantillas respecto a funciones sobrecargadas?**

A) Código menos comprensible
B) Evita duplicación de código para tipos distintos
C) Reduce la seguridad de tipos
D) Ocupa menos memoria en ejecución

53. **¿Qué ventaja presenta una implementación dinámica de lista frente a una estática?**

A) Acceso más rápido
B) Menor uso de punteros
C) Capacidad variable durante ejecución
D) Mejor integración con C++ moderno

54. **¿Qué solución evita errores al insertar un nodo al inicio de una lista dentro de una función?**

A) Usar NULL
B) Usar un puntero global
C) Usar punteros a punteros
D) Reservar más memoria

55. **¿Qué representa el conjunto de operaciones observadoras de un TAD?**

A) Creación de estructuras
B) Cambios de estado internos
C) Consultas sin modificar el estado
D) Acceso restringido

56. **¿Cuál es la función del constructor por defecto en C++?**

A) Inicializar con parámetros
B) No inicializar ningún valor
C) Inicializar con valores predeterminados automáticamente
D) Definir la herencia de una clase

57. **¿Qué hace este código?**

```cpp
lista<float> l(3.14);
cout << l.observarIzq();
```
A) Error de compilación
B) Imprime 0
C) Imprime 3.14
D) Accede a una posición inválida

58. **¿Qué ocurre si delete se aplica a un puntero nulo?**

A) Se lanza una excepción
B) Se produce un error de ejecución
C) No ocurre nada
D) Se bloquea el sistema

59. **¿Qué operador permite obtener el valor apuntado por un puntero?**

A) &
B) *
C) ->
D) %

60. **¿Qué hace esta función?**

```cpp
bool lista::esvacia() {
  return (n == 0);
}
```
A) Inserta un elemento
B) Devuelve true si la lista no tiene elementos
C) Elimina todos los elementos
D) Comprueba si hay espacio


61. **¿Qué hace este código?**

```cpp
int a = 10;
int *p = &a;
*p = *p + 5;
cout << a;
```
A) Imprime 10
B) Imprime 5
C) Imprime 15
D) Error de compilación

62. **¿Qué imprime este código?**

```cpp
int v[] = {2, 4, 6};
cout << *(v + 1) + *(v + 2);
```
A) 6
B) 10
C) 4
D) 2

63. **¿Qué ocurre si se omite el delete en estructuras dinámicas?**

A) Se libera memoria automáticamente
B) Se produce un error de compilación
C) Se genera una fuga de memoria
D) Se elimina parcialmente la estructura

64. **¿Qué significa seekp(0, ios::end)?**

A) Mueve el puntero al principio
B) Mueve el puntero de lectura al final
C) Mueve el puntero de escritura al final
D) No modifica la posición

65. **¿Qué hace este fragmento?**

```cpp
template <class T>
T cuadrado(T x) { return x * x; }
```
A) Calcula la raíz cuadrada
B) Multiplica x por 2
C) Retorna el cuadrado de x
D) Imprime x

66. **¿Qué error tiene este código?**

```cpp
ifstream f("archivo");
f.write("dato", 4);
```
A) ifstream no tiene método write
B) write requiere un entero
C) "dato" es constante
D) El archivo no se abre

67. **¿Qué produce este código?**

```cpp
int *p = new int[3];
p[0] = 1; p[1] = 2; p[2] = 3;
cout << *(p + 1);
```
A) 1
B) 2
C) 3
D) Error

68. **¿Cuál es el efecto de borrarLista(lista) si lista se pasa por puntero simple?**

A) Se libera la lista y el puntero original se pone a NULL
B) Se libera la lista pero el puntero original sigue apuntando a memoria inválida
C) El puntero se borra automáticamente
D) No se borra nada

69. **¿Qué hace este código?**

```cpp
TLista<int> l;
l.insertar(1, 4);
l.modificar(1, 9);
cout << l.observar(1);
```
A) 4
B) 9
C) 1
D) Error

70. **¿Qué condición es necesaria para acceder a un elemento de una lista genérica con observar(i)?**

A) i == 0
B) i >= 1 && i <= longitud()
C) i > longitud()
D) i < 1

71. **¿Qué situación puede justificar el uso de una lista doblemente enlazada?**

A) Acceso aleatorio
B) Recorriendo de fin a inicio
C) Menor complejidad
D) Evitar punteros

72. **¿Qué ventaja aporta el uso de template <class T> frente a funciones específicas?**

A) Reduce la necesidad de casting
B) Mejora la sintaxis
C) Evita usar punteros
D) Elimina operadores

73. **¿Qué tipo de error representa un doble delete?**

A) Sintáctico
B) Semántico
C) De ejecución (runtime)
D) De compilación

74. **¿Cuándo es necesario usar seekg(offset, ios::cur)?**

A) Para escribir desde el final
B) Para volver al principio del archivo
C) Para avanzar desde la posición actual
D) Para borrar el archivo

75. **¿Qué representa el género en la especificación algebraica?**

A) Un tipo de archivo
B) Un nombre para un tipo abstracto
C) Una constante
D) Una clase derivada

76. **¿Qué es una operación generadora en un TAD?**

A) Una que destruye estructuras
B) Una que observa atributos
C) Una que construye valores del tipo
D) Una que exporta datos

77. **¿Qué sucede si no se libera correctamente la memoria en TLista?**

A) Se borra automáticamente al salir del ámbito
B) Aparecen errores de compilación
C) Puede haber fuga de memoria
D) Se recorre la lista y se vacía

78. **¿Cuál es el propósito de template <class T> al inicio de una clase?**

A) Indicar que solo se usa int
B) Definir una clase con tipos genéricos
C) Heredar automáticamente
D) Evitar errores de puntero

79. **¿Cuál es el valor de posicion(9) si la lista contiene: 3, 9, 7?**

A) 0
B) 1
C) 2
D) -1

80. **¿Qué ocurre si se accede a elementos[100] cuando n = 10?**

A) Se accede al final de la lista
B) Se genera error de compilación
C) Se produce comportamiento indefinido
D) Devuelve NULL


81. **¿Qué hace este código?**

```cpp
float x = 2.0;
float *px = &x;
*px *= 3;
cout << x;
```
A) 2.0
B) 6.0
C) Error
D) Dirección de x

82. **¿Qué representa *(tabla + 2)?**

```cpp
int tabla[] = {10, 20, 30};
```
A) El primer elemento
B) El segundo elemento
C) El tercero (30)
D) Error

83. **¿Cuál es el resultado de este código?**

```cpp
TLista<int> l;
l.insertar(1, 5);
l.insertar(2, 10);
l.eliminar(1);
cout << l.observar(1);
```
A) 10
B) 5
C) -1
D) Error

84. **¿Cuál es el uso correcto de ofstream para añadir al final de un archivo?**

A) ofstream f("archivo", ios::binary);
B) ofstream f("archivo", ios::out);
C) ofstream f("archivo", ios::app);
D) ofstream f("archivo", ios::in);

85. **¿Qué ocurre si en TLista se intenta observar una posición no válida?**

A) Se retorna -1
B) Se lanza una excepción
C) Comportamiento indefinido
D) Se devuelve el último valor

86. **¿Qué hace este fragmento?**

```cpp
ifstream f("data", ios::binary);
char buffer[10];
f.read(buffer, 10);
```
A) Escribe 10 bytes en data
B) Lee 10 bytes de data y los guarda en buffer
C) Abre un archivo en texto
D) Cierra el archivo

87. **¿Qué sucede si se usa delete[] en lugar de delete?**

A) Nada
B) Libera correctamente la memoria
C) Puede provocar errores si no se usó new[]
D) Se produce error de compilación

88. **¿Qué hace este código?**

```cpp
cola c;
cout << c.esvacia();
```
A) Error de compilación
B) Imprime 1
C) Imprime 0
D) Lanza excepción

89. **¿Qué salida produce?**

```cpp
int arr[] = {5, 10, 15};
cout << arr[1];
```
A) 5
B) 10
C) 15
D) Error

90. **¿Qué implica declarar una clase con template <class T>?**

A) Que solo acepta int
B) Que es una clase base
C) Que se puede instanciar con diferentes tipos
D) Que no tiene métodos

91. **¿Cuándo es preferible usar una tabla dinámica en lugar de lista enlazada?**

A) Cuando se requiere acceso directo por índice
B) Cuando los elementos cambian constantemente
C) Cuando se recorre desde el final
D) Cuando se insertan elementos en medio

92. **¿Cuál es una desventaja de las listas enlazadas?**

A) Inserciones lentas
B) Mayor uso de memoria por nodo
C) Acceso directo
D) No permiten crecer dinámicamente

93. **¿Qué efecto puede tener una mala gestión del puntero elementos en una lista?**

A) Se produce una excepción
B) Se sobreescribe memoria ajena
C) Se pierden referencias a los nodos
D) Mejora el rendimiento

94. **¿Cuándo es útil posicion(e) en una lista?**

A) Cuando no se necesita recorrer la lista
B) Para saber cuántos elementos tiene
C) Para localizar la posición de un valor
D) Para eliminar el primer nodo

95. **¿Qué es una especificación algebraica?**

A) Implementación concreta de una clase
B) Definición formal de un TAD con operaciones y ecuaciones
C) Declaración de estructuras de memoria
D) Representación en lenguaje ensamblador

96. **¿Qué caracteriza a una operación modificadora?**

A) Devuelve un valor sin modificar el TAD
B) Crea un nuevo TAD
C) Cambia el estado interno del TAD
D) Observa un valor

97. **¿Cuál es la salida de este código?**

```cpp
int x = 3;
int *p = &x;
cout << *p + 1;
```
A) 3
B) 4
C) Dirección de x
D) Error

98. **¿Qué hace esta clase?**

```cpp
template <class T>
class TLista {
  // ...
};
```
A) Define una lista de enteros
B) Define una clase abstracta
C) Define una clase genérica parametrizada por tipo
D) Define una macro

99. **¿Qué hace el operador ->?**

A) Crea un puntero
B) Borra un puntero
C) Accede a un miembro de un objeto apuntado por puntero
D) Multiplica dos valores

100. **¿Qué valor retorna longitud() al crear una lista vacía?**

A) -1
B) 0
C) 1
D) Depende del sistema


101. **¿Qué hace el siguiente código?**

```cpp
int *p = new int;
*p = 42;
delete p;
cout << *p;
```
A) Imprime 42
B) Error de compilación
C) Comportamiento indefinido
D) Imprime 0

102. **¿Qué produce el siguiente fragmento?**

```cpp
float datos[] = {1.0, 2.0, 3.0};
cout << *(datos + 1);
```
A) 1.0
B) 2.0
C) 3.0
D) Error

103. **¿Qué hace el siguiente código en una lista genérica?**

```cpp
TLista<int> l;
l.insertar(1, 8);
l.insertar(2, 6);
l.eliminar(2);
cout << l.longitud();
```
A) 0
B) 1
C) 2
D) Error

104. **¿Qué ocurre al ejecutar este código?**

```cpp
ifstream entrada("datos.txt");
entrada << "Texto";
```
A) Escribe “Texto” en el archivo
B) Error en tiempo de ejecución
C) No compila
D) No hace nada

105. **¿Qué realiza esta operación?**

```cpp
cola c;
c.encolar("A");
c.desencolar();
cout << c.esvacia();
```
A) Error de compilación
B) Imprime 0
C) Imprime 1
D) Elimina el primer nodo y lo imprime

106. **¿Cuál es el objetivo de seekp(0, ios::beg)?**

A) Posicionar el puntero de lectura al principio
B) Posicionar el puntero de escritura al principio
C) Leer desde el final
D) Truncar el archivo

107. **¿Qué ocurre al hacer delete[] sobre un puntero NULL?**

A) Error
B) Nada
C) Se reinicia el sistema
D) Se imprime un warning

108. **¿Cuál es el resultado de esta secuencia?**

```cpp
TLista<int> l;
l.insertar(1, 5);
l.insertar(2, 10);
l.modificar(2, 20);
cout << l.observar(2);
```
A) 10
B) 5
C) 20
D) -1

109. **¿Qué hace tellg()?**

A) Posiciona el puntero de escritura
B) Devuelve la posición actual de lectura
C) Devuelve el tamaño del archivo
D) Lee una línea de texto

110. **¿Qué imprime este código?**

```cpp
int x = 4;
int *p = &x;
*p += 2;
cout << x;
```
A) 2
B) 4
C) 6
D) Dirección de x

111. **¿Cuándo es mejor una cola circular con vector que una con nodos enlazados?**

A) Cuando no se conocen los límites de crecimiento
B) Cuando se requiere eficiencia y tamaño acotado
C) Cuando se necesita recorrer hacia atrás
D) Cuando se eliminan elementos aleatorios

112. **¿Qué ventaja tienen las plantillas sobre las funciones específicas?**

A) Mejor integración con librerías
B) Evitan redundancia de código
C) Requieren menos compilación
D) Funcionan sin tipos

113. **¿Por qué se recomienda definir métodos de clases genéricas en el .h?**

A) Porque así los reconoce el compilador
B) Porque el .cpp no permite plantillas
C) Porque los compiladores no pueden instanciarlos si no están visibles
D) Por ahorro de memoria

114. **¿Qué problema puede surgir con listas genéricas si no se especializa una operación?**

A) Se borra el tipo
B) El compilador lanza error de ambigüedad
C) El operador puede no estar definido para ese tipo
D) No se compila la clase

115. **¿Cuál es el propósito de una operación constructora en un TAD?**

A) Eliminar el contenido
B) Consultar información
C) Generar un valor del tipo definido
D) Validar datos

116. **¿Cuál es el dominio de una operación parcial?**

A) Ninguno
B) Solo valores constantes
C) Solo el conjunto vacío
D) El subconjunto donde está definida la operación

117. **¿Qué ocurre si se accede a una posición no válida en una tabla dinámica?**

A) Se lanza excepción
B) Se ajusta el índice automáticamente
C) Comportamiento indefinido
D) Se inserta 0

118. **¿Qué operador se utiliza para declarar un puntero?**

A) &
B) *
C) ->
D) %

119. **¿Qué hace esvacia() en una lista?**

A) Devuelve el número de elementos
B) Borra todos los elementos
C) Devuelve si la lista tiene cero elementos
D) Imprime los nodos

120. **¿Cuál es el valor de posicion(7) si 7 no está en la lista?**

A) 0
B) -1
C) 1
D) Error


121. **¿Qué salida produce el siguiente código?**

```cpp
int a = 3, b = 5;
int *p = &a, *q = &b;
*p = *q;
cout << a;
```
A) 3
B) 5
C) Dirección de b
D) Error de compilación

122. **¿Qué hace este fragmento de código?**

```cpp
float *tabla = new float[3];
tabla[1] = 2.5;
cout << tabla[1];
```
A) Imprime 0
B) Imprime dirección de memoria
C) Imprime 2.5
D) Error de compilación

123. **¿Qué realiza esta función?**

```cpp
bool lista::esvacia() {
  return (n == 0);
}
```
A) Vacía la lista
B) Comprueba si la lista está vacía
C) Devuelve true si la lista tiene elementos
D) Inserta un elemento

124. **¿Qué ocurre si se accede a una posición inexistente con observar(i)?**

A) Se devuelve NULL
B) Se imprime 0
C) Se accede a memoria inválida
D) Se corrige automáticamente

125. **¿Qué hace este código?**

```cpp
ifstream entrada("datos.bin", ios::binary);
entrada.seekg(0, ios::end);
int tam = entrada.tellg();
```
A) Borra el fichero
B) Calcula el número de registros
C) Obtiene el tamaño del fichero
D) Recorre el archivo desde el principio

126. **¿Qué implica el uso de delete[]?**

A) Liberar un puntero simple
B) Liberar memoria asignada con new[]
C) Asignar un puntero a NULL
D) Declarar un puntero

127. **¿Qué salida produce el siguiente código?**

```cpp
TLista<int> lista;
lista.insertar(1, 3);
lista.modificar(1, 9);
cout << lista.observar(1);
```
A) 3
B) 9
C) Error
D) 0

128. **¿Qué ocurre si se llama modificar(i, elto) con i fuera de rango?**

A) Se inserta en la última posición
B) Se produce un error de compilación
C) Comportamiento indefinido
D) El elemento se ignora

129. **¿Qué representa esta definición?**

```cpp
template <class T>
class TLista { /* ... */ };
```
A) Una clase abstracta
B) Una clase concreta para enteros
C) Una clase genérica parametrizada por tipo
D) Una macro

130. **¿Qué hace esta función genérica?**

```cpp
template <typename T>
T mayor(T a, T b) {
  return (a < b) ? b : a;
}
```
A) Compara dos enteros
B) Retorna el menor
C) Retorna el mayor de dos valores
D) No compila

131. **¿Qué ventaja ofrece una lista enlazada frente a un array para inserciones?**

A) Acceso más rápido por índice
B) Inserción más eficiente en cualquier punto
C) Menor uso de memoria
D) Mayor velocidad de recorrido

132. **¿Cuál es un inconveniente de las listas dinámicas frente a las tablas?**

A) No pueden crecer
B) No pueden liberar memoria
C) Requieren más memoria por nodo
D) Son más difíciles de recorrer

133. **¿Cuándo es preferible usar seekp en vez de seekg?**

A) Al leer una posición
B) Para consultas sobre el tamaño del fichero
C) Al escribir en una posición específica
D) Para borrar datos

134. **¿Por qué no conviene separar las implementaciones de métodos de clases plantilla en archivos .cpp?**

A) Porque ralentiza la ejecución
B) Porque no compilan
C) Porque el compilador necesita ver el código fuente completo para instanciar la plantilla
D) Porque requieren main() en el mismo fichero

135. **¿Qué es una operación observadora en la especificación de un TAD?**

A) Una operación que modifica el estado
B) Una operación que crea un valor
C) Una operación que devuelve información sin modificar el estado
D) Una operación que inicializa atributos

136. **¿Qué es una operación modificadora?**

A) Una que elimina un TAD
B) Una que cambia el estado del TAD
C) Una que solo consulta
D) Una que convierte un tipo en otro

137. **¿Qué ocurre al hacer delete de un puntero nulo?**

A) Se lanza excepción
B) Se libera sin problema
C) Error de compilación
D) Se produce fuga de memoria

138. **¿Qué hace el operador * en la línea int *p = &x;?**

A) Multiplica
B) Declara un puntero a entero
C) Asigna el valor de x
D) Desreferencia automáticamente

139. **¿Qué operador permite acceder a un miembro desde un puntero a objeto?**

A) .
B) &
C) ->
D) *

140. **¿Qué devuelve longitud() en una lista con 4 elementos?**

A) 4
B) 3
C) 1
D) -1


141. **¿Qué ocurre si se hace delete[] p cuando p fue asignado con new (sin corchetes)?**

A) Error de compilación
B) Se libera correctamente
C) Comportamiento indefinido
D) El compilador ignora la operación

142. **¿Qué resultado se obtiene?**

```cpp
int v[] = {2, 4, 6};
int *p = v;
cout << *(p + 2);
```
A) 2
B) 4
C) 6
D) Dirección de v[2]

143. **¿Qué hace este código?**

```cpp
cola c;
c.encolar("dato");
c.desencolar();
cout << c.esvacia();
```
A) Imprime 1
B) Imprime 0
C) Error de compilación
D) Inserta un nuevo elemento

144. **¿Qué devuelve longitud() inmediatamente después de crear una lista?**

A) 0
B) 1
C) -1
D) NULL

145. **¿Qué representa &variable?**

A) Valor de la variable
B) Puntero nulo
C) Dirección de memoria de la variable
D) El contenido apuntado

146. **¿Qué resultado da este fragmento?**

```cpp
TLista<float> lista;
lista.insertar(1, 1.1);
cout << lista.observar(1);
```
A) 0
B) 1.1
C) Error
D) NULL

147. **¿Cuál es el efecto de seekg(0, ios::beg)?**

A) Posiciona al final
B) Posiciona al inicio del fichero para lectura
C) Borra el fichero
D) Cierra el fichero

148. **¿Qué ocurre si delete se llama sobre una dirección liberada previamente?**

A) Se borra nuevamente
B) Se imprime 0
C) Comportamiento indefinido
D) El compilador lo impide

149. **¿Qué hace template <typename T> en una función?**

A) Limita a tipos enteros
B) Crea múltiples copias en memoria
C) Permite usar la función con diferentes tipos
D) Impide usar funciones virtuales

150. **¿Qué valor retorna posicion(5) si 5 es el segundo elemento?**

A) 0
B) 1
C) 2
D) -1

151. **¿Cuál es el principal inconveniente de usar arrays para colas?**

A) No permiten inserciones
B) Redimensionamiento costoso o uso limitado si tamaño fijo
C) No permiten acceso por índice
D) No se puede borrar elementos

152. **¿Cuál es la ventaja de las listas enlazadas para colas?**

A) Acceso aleatorio
B) Menor uso de memoria
C) Crecimiento dinámico sin límites predefinidos
D) Velocidad de recorrido

153. **¿Cuándo conviene usar plantillas de clase?**

A) Si solo se trabaja con enteros
B) Cuando se requiere generalidad en los tipos
C) Cuando se necesita herencia múltiple
D) Solo en algoritmos matemáticos

154. **¿Qué puede fallar al usar mayor(a, b) con un tipo T personalizado?**

A) Error de compilación por tipo no definido
B) El operador < no está sobrecargado para T
C) T debe ser int
D) a y b deben ser referencias

155. **¿Qué es una especificación algebraica?**

A) Un código fuente
B) Una representación interna en memoria
C) Una definición formal de tipos y operaciones
D) Una notación gráfica

156. **¿Qué diferencia a una operación generadora?**

A) Modifica el TAD
B) Retorna información sin modificar
C) Produce valores del tipo definido
D) No requiere argumentos

157. **¿Qué hace este código?**

```cpp
int x = 4;
int *p = &x;
cout << *p + 2;
```
A) 6
B) 4
C) Error
D) Dirección de x

158. **¿Qué imprime?**

```cpp
int datos[4] = {10, 20, 30, 40};
cout << *(datos + 3);
```
A) 10
B) 20
C) 30
D) 40

159. **¿Qué sucede al escribir en un fichero abierto como ifstream?**

A) Se escribe correctamente
B) Se lanza excepción
C) Error de compilación
D) No se permite, ifstream es de solo lectura

160. **¿Qué resultado da este fragmento?**

```cpp
TLista<int> l;
l.insertar(1, 10);
l.eliminar(1);
cout << l.esvacia();
```
A) 0
B) 1
C) -1
D) Error


161. **¿Qué ocurre si se hace delete sobre un puntero que apunta a una dirección ya liberada?**

A) El puntero se convierte en NULL
B) Se libera de nuevo correctamente
C) Comportamiento indefinido
D) El compilador lo impide

162. **¿Qué hace este código?**

```cpp
int *p = new int[3];
p[0] = 10; p[1] = 20; p[2] = 30;
cout << *(p + 1);
```
A) 10
B) 20
C) 30
D) Error

163. **¿Qué imprime este código?**

```cpp
TLista<int> lista;
lista.insertar(1, 4);
lista.insertar(2, 8);
lista.eliminar(1);
cout << lista.observar(1);
```
A) 4
B) 8
C) 0
D) -1

164. **¿Qué hace este fragmento?**

```cpp
ifstream f("datos", ios::binary);
f.seekg(0, ios::end);
int tam = f.tellg();
```
A) Posiciona el cursor al principio
B) Escribe al final del archivo
C) Devuelve el tamaño del archivo
D) Mueve el cursor a una línea específica

165. **¿Qué sucede al llamar a esvacia() sobre una lista recién creada?**

A) Retorna 1
B) Retorna 0
C) Retorna -1
D) Error de compilación

166. **¿Qué significa *p = *q; si p y q son punteros?**

A) Se copia el valor apuntado por q en la dirección a la que apunta p
B) p pasa a apuntar a q
C) q se convierte en NULL
D) Se intercambian los punteros

167. **¿Qué hace este fragmento?**

```cpp
ofstream f("datos", ios::binary | ios::app);
f.write((char*)&x, sizeof(x));
```
A) Lee datos de un archivo
B) Sobrescribe el archivo desde el principio
C) Añade los datos binarios de x al final del archivo
D) Imprime x en pantalla

168. **¿Qué imprime este código?**

```cpp
int x = 5;
int *p = &x;
cout << (*p)++;
```
A) 5
B) 6
C) Error
D) Dirección de x

169. **¿Cuál es la utilidad del operador ->?**

A) Multiplicación
B) Asignación
C) Acceder a un miembro a través de un puntero
D) Comparación

170. **¿Qué valor retorna posicion(8) si 8 no está en la lista?**

A) 0
B) -1
C) NULL
D) Error

171. **¿Cuál es una ventaja clave de las tablas dinámicas frente a las listas?**

A) Inserciones más eficientes en cualquier lugar
B) Acceso aleatorio en tiempo constante
C) Menor uso de memoria
D) Eliminación más rápida

172. **¿Qué problema pueden presentar los arrays dinámicos al crecer?**

A) Se corrompen los datos
B) Hay que copiar todos los elementos a una nueva zona de memoria
C) No permiten borrado
D) No se pueden recorrer

173. **¿Cuándo se prefiere una lista doblemente enlazada?**

A) Para recorrer en ambos sentidos
B) Para ahorrar memoria
C) Para implementar vectores
D) Para evitar punteros

174. **¿Por qué es necesario definir métodos plantilla en el mismo archivo que la clase?**

A) Porque C++ no permite separarlos
B) Porque no se pueden compilar si están separados
C) Porque el compilador necesita ver el código fuente completo para instanciar la plantilla
D) Por eficiencia en ejecución

175. **¿Qué define una signatura en la especificación algebraica?**

A) La implementación del algoritmo
B) Los atributos internos de la clase
C) El conjunto de nombres y tipos de las operaciones
D) Las estructuras de control utilizadas

176. **¿Qué función tiene una operación observadora?**

A) Modifica el estado interno
B) Devuelve un valor sin alterar el estado
C) Elimina valores
D) Crea estructuras nuevas

177. **¿Qué hace el operador * en la instrucción int *p = &x;?**

A) Multiplica
B) Indica que p es un puntero
C) Asigna un valor
D) Libera memoria

178. **¿Qué produce este código?**

```cpp
int x = 7;
int *p = &x;
*p = *p + 2;
cout << x;
```
A) 7
B) 9
C) Error
D) Dirección de x

179. **¿Qué operador se usa para acceder a un campo de un objeto apuntado por puntero?**

A) .
B) *
C) ->
D) &

180. **¿Qué valor devuelve longitud() en una lista con 5 elementos?**

A) 0
B) 1
C) 5
D) -1


181. **¿Qué imprime este fragmento?**

```cpp
int a = 1, b = 2;
int *p = &a, *q = &b;
*p = *q + 3;
cout << a;
```
A) 2
B) 3
C) 5
D) Dirección de b

182. **¿Qué hace esta plantilla?**

```cpp
template <typename T>
T suma(T a, T b) {
  return a + b;
}
```
A) Suma solo enteros
B) Funciona con cualquier tipo que tenga definido +
C) Es una macro
D) Solo sirve para floats

183. **¿Qué devuelve este código?**

```cpp
TLista<int> l;
l.insertar(1, 10);
cout << l.observar(1);
```
A) 0
B) 10
C) -1
D) Error

184. **¿Qué hace este fragmento?**

```cpp
ifstream entrada("datos.txt");
entrada.seekg(0, ios::end);
long tam = entrada.tellg();
```
A) Posiciona al principio
B) Cierra el archivo
C) Lee el contenido del archivo
D) Obtiene el tamaño del archivo

185. **¿Qué pasa si se accede a una posición inválida en una tabla dinámica?**

A) Se devuelve -1
B) Se lanza una excepción
C) Comportamiento indefinido
D) Se detiene el programa

186. **¿Qué imprime este código?**

```cpp
int v[] = {1, 2, 3};
cout << *(v + 0);
```
A) 1
B) 2
C) 3
D) Error

187. **¿Qué hace el operador & en la línea int *p = &x;?**

A) Multiplica
B) Devuelve el valor
C) Devuelve la dirección de x
D) Declara un puntero

188. **¿Qué ocurre si se omite el delete de una lista dinámica?**

A) La memoria se libera automáticamente
B) El compilador lanza error
C) Se produce una fuga de memoria
D) La lista no se crea

189. **¿Qué resultado da este código?**

```cpp
int *p = new int(6);
cout << *p;
```
A) Dirección de p
B) 6
C) Error
D) NULL

190. **¿Qué hace cerrar() en un flujo?**

A) Cierra el archivo
B) Borra el archivo
C) Elimina el contenido
D) Imprime en consola

191. **¿Cuándo es más adecuada una pila con lista enlazada frente a vector?**

A) Cuando el tamaño es fijo
B) Cuando hay muchas operaciones top()
C) Cuando no se conoce el número de elementos previamente
D) Cuando se necesita acceso aleatorio

192. **¿Qué ventaja tiene una cola con vector circular frente a una lista?**

A) Menor uso de memoria por nodo
B) Mejor acceso a posiciones intermedias
C) Acceso en ambos extremos
D) Uso eficiente del espacio con tamaño acotado

193. **¿Qué situación obliga a usar template?**

A) Se requiere escribir varias funciones similares para tipos distintos
B) Se quiere usar variables globales
C) Se necesita depurar más rápido
D) Se accede a archivos binarios

194. **¿Qué ocurre si no se sobrecarga un operador requerido en una plantilla?**

A) La función se ejecuta sin errores
B) Se produce un error de compilación
C) El tipo se convierte a int
D) El compilador usa un operador por defecto

195. **¿Qué describe una especificación algebraica?**

A) La estructura física del TAD
B) Las estructuras dinámicas en memoria
C) Los tipos abstractos mediante operaciones y ecuaciones
D) La implementación exacta en C++

196. **¿Qué caracteriza a una operación parcial?**

A) Está definida para todos los valores posibles
B) Solo está definida para ciertos valores válidos del dominio
C) Se ejecuta siempre correctamente
D) No requiere argumentos

197. **¿Qué hace este código?**

```cpp
int *p = new int;
*p = 9;
cout << *p;
delete p;
```
A) Imprime 0
B) Imprime 9
C) Error
D) Imprime la dirección de p

198. **¿Qué resultado da este fragmento?**

```cpp
int a = 10;
int *p = &a;
cout << *(p + 1);
```
A) 10
B) Comportamiento indefinido
C) Error de compilación
D) 0

199. **¿Qué salida produce?**

```cpp
int x = 4;
int *p = &x;
(*p)++;
cout << x;
```
A) 3
B) 4
C) 5
D) Dirección de x

200. **¿Qué ocurre si no se actualiza el puntero externo tras borrar una lista?**

A) Nada
B) Se genera excepción
C) Queda apuntando a memoria liberada (puntero colgante)
D) Se borra automáticamente


## Soluciones y Explicaciones

1. C - Se accede fuera de los límites del array dinámico (tabla[3]), lo que produce comportamiento indefinido.
2. B - El puntero lista es pasado por valor, por lo que la modificación no afecta al puntero original fuera de la función.
3. C - Se incrementa el valor apuntado por p y valor pasa a 15.
4. C - seekg posiciona al final y tellg devuelve la posición, equivalente al tamaño del fichero.
5. C - Se modifica una copia del puntero; el original sigue apuntando a memoria liberada.
6. C - Retorna el mayor de los dos valores.
7. B - Lee un entero desde el fichero binario.
8. B - Usar delete[] con memoria reservada con new produce comportamiento indefinido.
9. C - seekg se usa para lectura y seekp para escritura.
10. B - La plantilla se instancia para string y concatena "Hola " y "mundo".
11. C - La lista simplemente enlazada permite insertar al principio en O(1).
12. D - Una lista simplemente enlazada evita redimensionamientos constantes.
13. D - Las tablas dinámicas requieren redimensionamientos al llenarse.
14. C - Una lista enlazada puede crecer sin límite predefinido.
15. C - Un TAD se define de forma abstracta e independiente de la implementación.
16. C - Una especificación algebraica define operaciones y ecuaciones sobre los tipos.
17. B - Tras insertar y eliminar, la lista queda vacía y esvacia() devuelve true (1).
18. B - Indica que la clase puede trabajar con diferentes tipos de datos.
19. C - Sin destructor, la memoria dinámica puede no liberarse.
20. B - El operador -> permite acceder a campos de una estructura apuntada por puntero.

21. C - NULL se evalúa como false, por lo que se imprime "Puntero nulo".
22. C - v + 1 apunta al segundo elemento del array, que vale 2.
23. B - seekg permite posicionarse para acceso directo aleatorio.
24. B - Insertar en la posición 10 está fuera de rango en una lista vacía.
25. B - clear() limpia las flags de error del flujo.
26. A - La plantilla se instancia con int y 3 * 4 = 12.
27. A - Si no se cierra, el contenido puede no guardarse correctamente.
28. C - El operador & obtiene la dirección de una variable.
29. D - El índice 3 es inválido si la lista está vacía.
30. C - Liberar dos veces produce comportamiento indefinido.
31. A - Una lista simplemente enlazada usa menos memoria por nodo.
32. B - Permite modificar el puntero principal desde la función.
33. C - Inserción y eliminación en la cima se realizan en O(1).
34. C - Las plantillas permiten reutilizar código para distintos tipos.
35. B - Una plantilla de función permite definir funciones genéricas.
36. C - Una operación observadora consulta sin modificar el TAD.
37. C - El operador -> accede a miembros desde un puntero a objeto.
38. B - read() lee bytes del fichero a la variable.
39. C - Existen varias definiciones con mismo nombre y distinta signatura.
40. B - Permite crear funciones independientes del tipo.

41. C - Usar delete[] sin haber usado new[] provoca comportamiento indefinido.
42. C - p + 2 apunta a v[2], que vale 30.
43. C - Una cola con nodos no tiene límite fijo de capacidad.
44. C - Retorna el menor de los dos valores.
45. C - El operador * permite acceder al contenido apuntado.
46. C - Puede provocar errores de doble liberación o fugas.
47. C - Se inserta 7 y luego se observa esa posición.
48. C - Desencolar en una cola vacía produce comportamiento indefinido si no se comprueba.
49. B - Posiciona al final y tellg devuelve el tamaño del archivo.
50. C - *pf desreferencia el puntero y muestra 3.5.
51. C - La lista doblemente enlazada permite recorrer en ambos sentidos.
52. B - Las plantillas evitan duplicar código para distintos tipos.
53. C - Una lista dinámica puede crecer o decrecer en ejecución.
54. C - Pasar punteros a punteros permite modificar el original.
55. C - Las observadoras consultan sin modificar el TAD.
56. C - El constructor por defecto inicializa con valores predeterminados.
57. C - Se crea la lista con un elemento 3.14 y se observa.
58. C - delete NULL es seguro y no hace nada.
59. B - El operador * obtiene el valor apuntado por el puntero.
60. B - Devuelve true si la lista no tiene elementos.

61. C - Se modifica a través del puntero y se imprime 15.
62. B - 4 + 6 = 10.
63. C - Omitir delete provoca fuga de memoria.
64. C - seekp mueve el puntero de escritura al final del archivo.
65. C - Retorna el cuadrado del valor.
66. A - ifstream no dispone de write.
67. B - *(p + 1) accede al segundo elemento, 2.
68. B - El puntero original queda apuntando a memoria liberada.
69. B - Se modifica el valor 4 por 9.
70. B - El índice debe estar entre 1 y longitud().
71. B - Permite recorrer de fin a inicio.
72. A - Reduce la necesidad de casting al usar plantillas.
73. C - Es un error de ejecución.
74. C - Desplaza desde la posición actual.
75. B - El género nombra el tipo abstracto.
76. C - Construye valores del TAD.
77. C - Si no se libera memoria, hay fuga.
78. B - Define una clase genérica.
79. C - 9 ocupa la segunda posición (cuenta desde 1).
80. C - Acceder más allá produce comportamiento indefinido.

81. B - *px *= 3 multiplica x por 3 y se imprime 6.0.
82. C - tabla + 2 apunta al tercer elemento (30).
83. A - Tras eliminar el primero, queda 10 en la posición 1.
84. C - ios::app abre para añadir al final.
85. C - Acceder a una posición no válida provoca comportamiento indefinido.
86. B - read lee 10 bytes en buffer.
87. C - delete[] debe emparejarse con new[]; de lo contrario puede fallar.
88. B - Una cola recién creada está vacía, esvacia() devuelve 1.
89. B - arr[1] vale 10.
90. C - La plantilla permite instanciar la clase con distintos tipos.
91. A - Las tablas permiten acceso directo por índice.
92. B - Cada nodo almacena un puntero adicional.
93. C - Se pierden referencias y la lista queda inconsistente.
94. C - posicion(e) localiza la posición de un valor.
95. B - Es la definición formal de un TAD.
96. C - Una operación modificadora altera el estado interno.
97. B - *p es 3, más 1 es 4.
98. C - Define una clase genérica.
99. C - -> accede a miembros de un objeto apuntado.
100. B - Una lista vacía tiene longitud 0.

101. C - Tras liberar la memoria, acceder a *p es indefinido.
102. B - *(datos + 1) vale 2.0.
103. B - Tras eliminar el segundo elemento, queda uno solo.
104. C - ifstream es solo lectura, por lo que no compila al usar <<.
105. C - Se encola y se desencola el único elemento, quedando la cola vacía.
106. B - seekp posiciona el puntero de escritura al principio.
107. B - delete[] sobre NULL no hace nada.
108. C - Se modifica el valor de la posición 2 a 20.
109. B - tellg devuelve la posición actual de lectura.
110. C - x se incrementa a 6.
111. B - Si el tamaño está acotado, un vector circular es más eficiente.
112. B - Las plantillas evitan redundancia de código.
113. C - El compilador necesita ver todo el código de la plantilla para instanciarla.
114. C - Si el operador no está definido para T, habrá error.
115. C - Las operaciones constructoras generan valores del TAD.
116. D - Una operación parcial solo está definida en un subconjunto del dominio.
117. C - Acceder fuera de rango produce comportamiento indefinido.
118. B - El asterisco declara un puntero.
119. C - esvacia devuelve true si la lista tiene cero elementos.
120. B - Si el elemento no está, posicion devuelve -1.

121. B - *p = *q copia el valor de b en a, por lo que imprime 5.
122. C - Se imprime 2.5 almacenado en la posición 1.
123. B - Devuelve true si la lista está vacía.
124. C - Acceder fuera de rango produce comportamiento indefinido.
125. C - Al posicionar al final, tellg devuelve el tamaño del fichero.
126. B - delete[] libera memoria reservada con new[].
127. B - Se modifica el valor a 9 y se observa.
128. C - Llamar modificar fuera de rango produce comportamiento indefinido.
129. C - Define una clase genérica parametrizada por tipo.
130. C - Devuelve el mayor valor comparando con <.
131. B - Las listas permiten inserción eficiente en cualquier punto.
132. C - Requieren más memoria por nodo debido a los punteros.
133. C - seekp reposiciona el puntero de escritura.
134. C - El compilador necesita ver la definición completa de la plantilla.
135. C - Una observadora devuelve información sin modificar el estado.
136. B - Una modificadora cambia el estado interno del TAD.
137. B - delete sobre un puntero nulo es seguro.
138. B - El asterisco en la declaración indica que es un puntero a entero.
139. C - El operador -> accede a un miembro a través de un puntero.
140. A - Una lista con 4 elementos tiene longitud 4.

141. C - delete[] debe emparejarse con new[]; de lo contrario es indefinido.
142. C - *(p + 2) accede al elemento 6.
143. A - Encolar y desencolar deja la cola vacía, por lo que esvacia() imprime 1.
144. A - Una lista recién creada tiene longitud 0.
145. C - El operador & obtiene la dirección de la variable.
146. B - Se inserta 1.1 y se observa correctamente.
147. B - Posiciona al inicio del fichero para lectura.
148. C - Liberar dos veces produce comportamiento indefinido.
149. C - Permite que la función sea genérica para distintos tipos.
150. C - Si 5 es el segundo elemento, la posición es 2.
151. B - Los arrays tienen tamaño fijo o requieren copias al redimensionar.
152. C - Las listas crecen dinámicamente sin límite predefinido.
153. B - Se usan plantillas cuando se requiere generalidad en los tipos.
154. B - Si T no define <, la plantilla mayor fallará al compilar.
155. C - Una especificación algebraica define tipos y operaciones formalmente.
156. C - Una operación generadora produce valores del tipo definido.
157. A - *p vale 4, sumando 2 se imprime 6.
158. D - *(datos + 3) accede a 40.
159. D - ifstream es de solo lectura y no permite escribir.
160. B - Tras insertar y eliminar, la lista queda vacía y esvacia() vale 1.

161. C - Liberar una dirección dos veces provoca comportamiento indefinido.
162. B - *(p + 1) vale 20.
163. B - Tras eliminar el primer elemento queda 8.
164. C - seekg al final y tellg devuelven el tamaño del archivo.
165. A - Una lista recién creada está vacía y esvacia() retorna 1.
166. A - Copia el valor apuntado por q en la dirección apuntada por p.
167. C - Se añaden los datos binarios de x al final del archivo.
168. A - Imprime 5 porque el post-incremento devuelve el valor previo.
169. C - El operador -> sirve para acceder a miembros desde un puntero.
170. B - Si el elemento no existe, posicion devuelve -1.
171. B - Las tablas permiten acceso aleatorio en tiempo constante.
172. B - Al crecer se debe copiar a una nueva zona de memoria.
173. A - Las listas dobles permiten recorrer en ambos sentidos.
174. C - El compilador necesita ver la plantilla completa en el archivo de cabecera.
175. C - La signatura especifica nombres y tipos de las operaciones.
176. B - Una observadora devuelve información sin alterar el estado.
177. B - El asterisco indica que p es un puntero.
178. B - x se incrementa a 9.
179. C - El operador -> permite acceder a campos a través de puntero.
180. C - Una lista con 5 elementos tiene longitud 5.

181. C - *p = *q + 3 asigna a a el valor de b + 3, resultando 5.
182. B - La plantilla funciona con cualquier tipo que tenga definido el operador +.
183. B - Se inserta 10 y se observa esa posición.
184. D - Posiciona al final y tellg devuelve el tamaño del archivo.
185. C - Acceder fuera de rango provoca comportamiento indefinido.
186. A - *(v + 0) accede al primer elemento, 1.
187. C - El operador & devuelve la dirección de x.
188. C - Omitir delete produce fuga de memoria.
189. B - Se crea un entero dinámico con valor 6 y se imprime.
190. A - close() cierra el archivo abierto.
191. C - Una lista enlazada permite crecer sin conocer el tamaño previamente.
192. D - El vector circular usa eficientemente un espacio fijo.
193. A - Las plantillas evitan escribir varias funciones para distintos tipos.
194. B - Si el operador requerido no existe, se produce error de compilación.
195. C - Describe tipos abstractos y operaciones mediante ecuaciones.
196. B - Una operación parcial solo está definida para algunos valores.
197. B - Se imprime 9 y luego se libera la memoria.
198. B - p + 1 apunta fuera del objeto; el resultado es indefinido.
199. C - El post-incremento modifica x a 5.
200. C - Si no se actualiza, queda como puntero colgante a memoria liberada.
