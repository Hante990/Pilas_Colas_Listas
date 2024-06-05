# Metodos_Numericos
<h2 align = "center"> <font color = "darkorange" size = "+6"  font face = "bauhaus 93">  Índice </font> </h2>
<header> <font color = "red" size="+1" font face = "aharoni">
                <nav class="navegacion">                   
     <li> <a href="#Descripcion"> Descripción </a> <br> </li>
                            <ul class="subindice"> 
                                <li> <a href="#Lineal"> Pilas (5 ejemplos). </a> </li>
                                <li> <a href="#Cuadratica"> Listas 5 ejemplo). </a> </li>
                                <li> <a href="#Langrage"> Colas(5 ejemplos). </a> </li> 
                            </ul>
                    </ul>
                </nav>
            </font> </header>

<h2 align = "center"> <font font face = "forte">  <a name="Descricpcion"> Descripción </a></h2>
Las estructuras lineales son colecciones de datos que se ordenan dependiendo de cómo se agregan o eliminan los elementos. Estas estructuras tienen dos extremos, que pueden llamarse "izquierda" y "derecha" o "frente" y "final", y se caracterizan por las operaciones de acceso y manipulación de los elementos.  
Existen varias estructuras lineales, cada uno con sus propias características y aplicaciones. Algunos de los más comunes son:
  <li>1.-Pilas </li>
  <li>2.-Listas</li>
  <li>3.-Colas</li>

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<h2 align = "center"> <font font face = "forte">  <a name="Lineal"> 1. Pilas  </a></h2>

<h3> <font font face = "arial"> DESCRIPCIÓN: </h3>

Las pilas son estructuras de datos lineales y dinámicas que siguen la política de Last-In, First-Out (LIFO), es decir, el último elemento que se agrega es el primero en ser eliminado. Estas estructuras tienen dos operaciones básicas: INSERTAR (llamada PUSH) y ELIMINAR (llamada POP)
<h3> Características</h3>
<li>Lineal: Los elementos se almacenan en una secuencia sucesiva en la memoria.</li>
<li>Dinámica: La pila puede crecer o disminuir en tamaño según se agreguen o eliminen elementos.</li>
<li>LIFO: El último elemento agregado es el primero en ser eliminado.</li>
<h3> Operaciones</h3>
<li>Crear: Se crea una pila vacía.</li>
<li>Destruir: Se elimina la pila y se libera la memoria asignada.</li>
<li>Insertar: Se agrega un nuevo elemento a la pila (llamada PUSH).</li>
<li>Eliminar: Se elimina el elemento superior de la pila (llamada POP).</li>
<li>Consultar el tope: Se obtiene el elemento superior de la pila.</li>
<h3>Implementación</h3>
Para implementar una pila, se utiliza una estructura de datos que consta de nodos, cada uno de los cuales contiene un valor y un apuntador al siguiente nodo. El apuntador del último nodo se establece en NULL para indicar el final de la pila.
<h3> Ejemplos</h3>
<li>Pila de libros: Una pila de libros en una librería, donde el último libro agregado es el primero en ser retirado.</li>
<li>Pila de platos: Una pila de platos en una cocina, donde el cocinero toma el plato superior (último agregado) para usarlo.</li>
<h3> Aplicaciones</h3>
<li>Evaluación de expresiones: Utilizarse para evaluar expresiones en postfijo.</li>
<li>Invertir elementos: Invertir los elementos de una pila.</li>
<li>Verificar palíndromos: Verificar si el contenido de una pila de caracteres es un palíndromo.</li>

![download](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/d20df356-065b-4953-b406-7c8b8caf1a63)

<h5> <font font face = "arial"> <b> <i> Ejemplo en código. </i> </b> </h5>

    class Node {
    int data;
    Node next;

    Node(int data) {
        this.data = data;
        next = null;
    }
    }

    class Stack {
    Node top;

    Stack() {
        top = null;
    }

    // Insertar un elemento en la pila
    void push(int data) {
        Node newNode = new Node(data);
        newNode.next = top;
        top = newNode;
    }

    // Eliminar y retornar el elemento en el tope de la pila
    int pop() {
        if (top == null) {
            System.out.println("Error: La pila está vacía");
            return -1;
        }
        int data = top.data;
        top = top.next;
        return data;
    }

    // Retornar el elemento en el tope de la pila sin eliminarlo
    int peek() {
        if (top == null) {
            System.out.println("Error: La pila está vacía");
            return -1;
        }
        return top.data;
    }

    // Verificar si la pila está vacía
    boolean isEmpty() {
        return top == null;
    }
    }

    public class Main {
    public static void main(String[] args) {
        Stack stack = new Stack();
        stack.push(10);
        stack.push(20);
        stack.push(30);
        System.out.println("Elemento eliminado: " + stack.pop());  // Salida: Elemento eliminado: 30
        System.out.println("Elemento en el tope: " + stack.peek());  // Salida: Elemento en el tope: 20
        System.out.println("¿La pila está vacía? " + stack.isEmpty());  // Salida: ¿La pila está vacía? false
    }
    }
    
![Screenshot 2024-06-05 080646](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/415ec603-3f0d-4245-b2ba-d7c5d638f858)

<h2 align = "center"> <font font face = "forte">  <a name="Cuadratica"> 2.- Listas  </a></h2>

<h3> <font font face = "arial"> DESCRIPCIÓN: </h3>

Las listas son estructuras de datos lineales y dinámicas que permiten almacenar y manipular conjuntos de elementos. Estas estructuras tienen varias características y operaciones básicas que las hacen útiles en muchos contextos de programación.
  <h3> Características</h3>
<li>Lineal: Los elementos se almacenan en una secuencia sucesiva en la memoria.</li>
<li>Dinámica: La lista puede crecer o disminuir en tamaño según se agreguen o eliminen elementos.</li>
<li>No necesariamente ordenada: Los elementos no necesariamente se ordenan en una secuencia específica.</li>
<h3> Operaciones Básicas</h3>
<li>Crear: Se crea una lista vacía.</li>
<li>Destruir: Se elimina la lista y se libera la memoria asignada.</li>
<li>Insertar: Se agrega un nuevo elemento en una posición específica.</li>
<li>Eliminar: Se elimina un elemento en una posición específica.</li>
<li>Consultar: Se obtiene el elemento en una posición específica.</li>
<h3> Tipos de Listas</h3>
<li>Listas enlazadas: Cada elemento es un nodo que contiene un valor y un apuntador al siguiente nodo.</li>
<li>Listas dinámicas: La lista puede crecer o disminuir en tamaño según se agreguen o eliminen elementos.</li>
<li>Listas estáticas: La lista tiene un tamaño fijo y no puede crecer o disminuir.</li>
<h3> Aplicaciones</h3>
<li>Almacenamiento de datos: Utilizarse para almacenar conjuntos de datos que necesitan ser accedidos y manipulados.</li>
<li>Estructuras de datos complejas: Utilizarse para crear estructuras de datos más complejas, como árboles y grafos.</li>
<li>Algoritmos de búsqueda y ordenamiento: Utilizarse en algoritmos de búsqueda y ordenamiento para manipular conjuntos de datos.</li>
<h3> Ventajas</h3>
<li>Flexibilidad: Las listas pueden crecer o disminuir en tamaño según sea necesario.</li>
<li>Eficiencia: Las listas pueden ser implementadas de manera eficiente en términos de memoria y tiempo de ejecución.</li>
<li>Facilidad de uso: Las listas son fáciles de implementar y utilizar en muchos contextos de programación.</li>
<h3> Desventajas</h3>
<li>Complejidad: Las listas pueden ser complejas de implementar y manejar, especialmente en grandes conjuntos de datos.</li>
<li>Tiempo de ejecución: Las operaciones de inserción y eliminación pueden ser lentas en listas grandes.</li>

![download](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/203c88db-b4c1-4dac-b7b9-dc091ae7a61e)

<h5> <font font face = "arial"> <b> <i> Ejemplo en código. </i> </b> </h5>

    class Node {
    int data;
    Node next;

    Node(int data) {
        this.data = data;
        next = null;
    }
    }

    class LinkedList {
    Node head;

    LinkedList() {
        head = null;
    }

    // Insertar un elemento en la lista
    void insert(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
        } else {
            Node current = head;
            while (current.next != null) {
                current = current.next;
            }
            current.next = newNode;
        }
    }

    // Eliminar un elemento en la lista
    void remove(int data) {
        if (head == null) {
            System.out.println("Error: La lista está vacía");
            return;
        }
        if (head.data == data) {
            head = head.next;
            return;
        }
        Node current = head;
        while (current.next != null) {
            if (current.next.data == data) {
                current.next = current.next.next;
                return;
            }
            current = current.next;
        }
        System.out.println("Error: El elemento no se encontró en la lista");
    }

    // Consultar un elemento en la lista
    int get(int index) {
        if (head == null) {
            System.out.println("Error: La lista está vacía");
            return -1;
        }
        Node current = head;
        int count = 0;
        while (current != null) {
            if (count == index) {
                return current.data;
            }
            count++;
            current = current.next;
        }
        System.out.println("Error: El índice no es válido");
        return -1;
    }

    // Verificar si la lista está vacía
    boolean isEmpty() {
        return head == null;
    }
    }

    public class Main {
    public static void main(String[] args) {
        LinkedList list = new LinkedList();
        list.insert(10);
        list.insert(20);
        list.insert(30);
        System.out.println("Elemento en la posición 1: " + list.get(1));  // Salida: Elemento en la posición 1: 20
        list.remove(20);
        System.out.println("¿La lista está vacía? " + list.isEmpty());  // Salida: ¿La lista está vacía? false
    }
    }
    
![Screenshot 2024-06-05 081304](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/4df9e003-7d60-4652-b46c-8adf3f9b9661)

<h2 align = "center"> <font font face = "forte"> <a name="Langrage">  3.- Colas  </a></h2>

<h3> <font font face = "arial"> DESCRIPCIÓN: </h3>

Una cola es una estructura de datos lineal y dinámica que sigue la política de First-In, First-Out (FIFO), es decir, el primer elemento agregado es el primero en ser eliminado. Las colas se utilizan para almacenar y manejar conjuntos de elementos de manera ordenada y eficiente.   
<h3>Características</h3>
<li>Lineal: Los elementos se almacenan en una secuencia sucesiva en la memoria.</li>
<li>Dinámica: La cola puede crecer o disminuir en tamaño según se agreguen o eliminen elementos.</li>
<li>FIFO: El primer elemento agregado es el primero en ser eliminado.</li>
<h3>Operaciones Básicas</h3>
<li>Crear: Se crea una cola vacía.</li>
<li>Destruir: Se elimina la cola y se libera la memoria asignada.</li>
<li>Insertar: Se agrega un nuevo elemento al final de la cola.</li>
<li>Eliminar: Se elimina el primer elemento de la cola.</li>
<li>Consultar: Se obtiene el primer elemento de la cola sin eliminarlo.</li>
<h3>Implementación</h3>
Las colas se pueden implementar utilizando diferentes estructuras de datos, como listas enlazadas o arreglos. La implementación más común es utilizando listas enlazadas, donde cada nodo contiene un valor y un apuntador al siguiente nodo.
<h3>Ventajas</h3>
<li>Flexibilidad: Las colas pueden crecer o disminuir en tamaño según sea necesario.</li>
<li>Eficiencia: Las colas pueden ser implementadas de manera eficiente en términos de memoria y tiempo de ejecución.</li>
<li>Facilidad de uso: Las colas son fáciles de implementar y utilizar en muchos contextos de programación.</li>
<h3>Desventajas</h3>
<li>Complejidad: Las colas pueden ser complejas de implementar y manejar, especialmente en grandes conjuntos de datos.</li>
<li>Tiempo de ejecución: Las operaciones de inserción y eliminación pueden ser lentas en colas grandes.</li>
<h3>Aplicaciones</h3>
<li>Almacenamiento de datos: Utilizarse para almacenar conjuntos de datos que necesitan ser accedidos y manipulados.</li>
<li>Estructuras de datos complejas: Utilizarse para crear estructuras de datos más complejas, como árboles y grafos.</li>
<li>Algoritmos de búsqueda y ordenamiento: Utilizarse en algoritmos de búsqueda y ordenamiento para manipular conjuntos de datos.</li>
<h3>Ejemplos</h3>
<li>Cola de impresión: Una cola de impresión es un ejemplo común de cola, donde los elementos se agregan al final y se eliminan del principio.</li>
<li>Cola de tareas: Una cola de tareas es otra aplicación común, donde los elementos se agregan al final y se eliminan del principio según sea necesario.</li>

  ![download](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/a1e1edd6-8b1c-4f74-9c9e-992d636f1c14)

<h5> <font font face = "arial"> <b> <i> Ejemplo en código. </i> </b> </h5>

     import java.util.LinkedList;

    public class Main {
    public static void main(String[] args) {
        LinkedList<Integer> queue = new LinkedList<>();
        queue.add(1);
        queue.add(2);
        queue.add(3);
        System.out.println(queue.poll()); // Salida: 1
        System.out.println(queue.peek()); // Salida: 2
    }
    }

![Screenshot 2024-06-05 081454](https://github.com/Hante990/Pilas_Colas_Listas/assets/107586879/d9804c00-40dc-4eb9-ab36-48d7556d7d76)

