    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h3>¿Que es una variable y para que sirve?</h3>
        <p> R//: Un espacio que reservamos en memoria.sirve para guardar un valor. 
            El valor puede ser cualquier tipo de dato, inclusive objetos o funciones.</p>

        <h3>¿Cual es la diferencia entre declarar e inicializar una variable?</h3>
        <p>R//:
            cuando la declaramos le estamos dando un nombre a la variable sea de tipo (let o const ) 
            (let nombre )  y cuando la inicializamos  es   que le damos el valor o dato (="Estefania").
            let nombre = "Estefania"</p>
            
        <h3> ¿Cual es la diferencia entre sumar numero y concatenar string </h3>
        <p>R //
             Para ambos se utiliza el signo + , sin embargo 2 + 2 = 4 pero cuando concatenamos estamos
             diciendo que esa palabra va junta "Estefania "  + "Villan"  = Estefania Villan</p>

        <h3> ¿ Cual operador me permite sumar o concatenar ?</h3>
        <p> + </p>

        <h3> Determina el nombre y tipo de dato para almacenar en variables.</h3>
        <p>R //:
        <ul>
            <li>Nombre = string</li>
            <li>Apellido = string</li>
            <li> Nombre de usuario en platzi = string</li>
            <li> Edad = number</li>
            <li> Correo electronico = string</li>
            <li> Mayor de edad = boolean</li>
            <li>Dinero ahorrado = number</li>
            <li> Deudas = number</li>
        </ul>
    </p>
    <h3>Traduce a codigo JS las variables del ejemplo anterior</h3>
    <p> R//: 
        let nombre = "Estefania"; <br>
        let apellido = "Villan";<br>
        let nombreDeUsuarioEnPlazi = "EstefaniaVillan";<br>
        let correoElectronico = "niavillan@gmail.com";<br>
        let mayorDeEdad = "true" <br>
        let dineroAhorrado = 1.000.000;<br>
        let deudad = 3.000.000;
    </p>

    <h3>Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior </h3>
    <ol>
        <li>Nombre completo (Nombre y apellido)</li>
        <li>Dinero real (Dinero ahorrado - deudas)</li>
    </ol>
    <p>R//:
        Primera forma
        let nombre = "Estefania";
        let apellido = "Villan";
        console.log("Estefania " + "Villan")

        Segunda forma
        let nombreCompleto = nombre + " " + apellido;

        Primera Forma
        let dineroAhorrado = 1000000;
        let deuda = 3000000;
        let total = dineroAhorrado - deuda;

        console.log( "Dinero en total " + total )

        Segunda forma
        let total = dineroAhorrado - deuda;

    </p>

    <h3>¿Que es una funcion?</h3>
    <p>R//: Es un bloque de codigo que usamos para encapsular o guardar bloques de codigo que vamos a reutilizar</p>

    <h3>¿Cuando me sirve usar una funcion en mi codigo?</h3>
    <p> R//: cuando tenemos variables o bloques de codigo muy parecido (con cambios que podrian ser parametros )
        que podemos encapsular para reutilizar as de una vez en el futuro.
    
    Tambien nos sirve para mejorar la legibilidad del codigo</p>

    <h3> ¿Cual es la diferencia entre parametro y argumentos en una funcion?</h3>
    <p> 
        Las funciones reciben parametros cuando las creamos , y les enviamos argumentos cuando las ejecutamos.

        Ejemplo 
        En la función 'sumar(x, y)' 'x' e 'y' son parámetros.
        Cuando llamas a la función con 'sumar(3, 5)', 3 y 5 son argumentos que se asignan 
        a los parámetros 'x' e 'y'.</p>

    <h3>Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes 
        por parámetros y argumentos en una función:
        const name = "Juan David";
        const lastname = "Castro Gallego";
        const completeName = name + lastname;
        const nickname = "juandc";
        
        console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + "."); </h3>

        <p> 
        R//: function saludo (name, lastname, nickname) {
                const completeName = nombreCompleto (name, lastname);
                console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
            }
            informacion("Juan David", "Castro Gallego", "juandc")
        </p>

        <h3>¿Que es un condicional</h3>
        <p>R//: Es la forma en que ejecutamos bloques de codigo dependendiendo la condicion</p>

        <h3>¿Que tipos de condicionales existen y cuales son sus diferencias?</h3>
        <p> if , elseif, else , switch.
        
        -if evalúa si una expresión o condición es verdadera. 
        Si lo es, realiza las instrucciones del bloque de código correspondiente.
        Si no lo es, sigue evaluando las demás condiciones (else if).
        Finalmente, si ninguna condición es verdadera, el bloque de código del final (else) se ejecuta.

        Ejemplo
        let edad = 18;
        if (edad >= 18){
            console.log("Puedes conducir")
        }
        
        Ejemplo
        let edad = 20;
        if (edad > 17 && edad <= 20){
            console.log("Eres joven");
            }else{
                console.log("No eres joven");
                }

    <!---(&&) valida si ambos son verdaderos -->

    -switch se utiliza para tomar decisiones basadas en el valor de una expresión.
    Se compara uno a uno todos los posibles casos hasta encontrar uno coincidente.
    Luego de encontrarlo, solo se ejecuta el bloque de código correspondiente al caso coincidente.
    Si no hay coincidencia con ninguno de los casos, se puede definir un default opcional.

            Ejemplo
            let dia = "lunes";
                switch (dia) {
                case "lunes":
                    console.log("Comienza la semana");
                    break;
                case "viernes":
                    console.log("¡Viernes, al fin!");
                    break;
                default:
                    console.log("Otros días de la semana");
                }
        </p>
    <h3>¿Puedo convinar funciones y condicionales?</h3>
    <p>Si. Las funciones pueden encapsular cualquier bloque de codigo incluyendo condicionales.
        Ademas, los condicionales pueden ser utilizados dentro de funciones.
    Ejemplo
    function mostrarMensaje(condicion){
        if (condicion == true){
            return "Es verdadero"
            }else{
                return "Es falso"
                }
                }
                console.log(mostrarMensaje(true)) // Es verdadero
                console.log(mostrarMensaje(false))// Es falso
                </p>


    <h3>Replica el comportamiento del siguiente codigo que usa la sentencia switch utilizando if, else y else if

        const tipoDeSuscripcion = "Basic";

        switch (tipoDeSuscripcion) {
    case "Free":
        console.log("Solo puedes tomar los cursos gratis");
        break;
    case "Basic":
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        break;
    case "Expert":
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        break;
    case "ExpertPlus":
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        break;
    }</h3>

    <p> R//:    
        
        const tipoDeSuscripcion = "Basic";

        if (tipoDeSuscripcion === "Free"){
            console.log("Solo puedes tomar los cursos gratis");
            } else if (tipoDeSuscripcion === "Basic"){
                console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
                } else if (tipoDeSuscripcion === "Expert"){
                    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
                    } else if (tipoDeSuscripcion === "ExpertPlus"){
                        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
                        }


                </p>

    <h3>Replica el comportamiento solo con if</h3>
    <p> R//:
        const tipoDeSuscripcion = "Basic";

        if(tipoDeSuscripcion === "Free"){
            console.log("Solo puedes tomar los cursos gratis");
        }

        if(tipoDeSuscripcion === "Basic"){
            console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        }

        if(tipoDeSuscripcion === "Expert"){
            console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        }
        
        if(tipoDeSuscripcion === "ExpertPlus"){
            console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        }

//otra opcion 
        const tipoDeSuscripcion = {
            free: "Solo puedes tomar los cursos gratis ",
            basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
            expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
            expertplus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
        }



    </p>       

    <h3>¿Que es un ciclo?</h3>
    <p> La forma de ejecutar un bloque de código varias veces mientras se cumpla una condición específica. </p>

    <h3>¿Que tipos de ciclos existen?</h3>
    <p> 
    - Ciclo for
    - Ciclo while
    - Ciclo do-while

        -ciclo for: nos pide que inicialicemos una variable la validacion y luego que hacemos 

        Ejemplo
        for (let i = 1; i <= 5; i++) {
            console.log("el valor de i es:" + i);
        }

        -ciclo while: hace la validacion antes de preguntar.  se repite mientras la condición sea verdadera, es decir, mientras que la condición no cambie a false 
        Ejemplo
        let i=0;
        while (i < 5) {
            console.log("El valor de i es :" + i);
            i++;
            }

        -ciclo do while:Es similar a while pero la diferencia que en este caso, primero se ejecuta el bloque
        de codigo y luego se verifica si sigue o no la condicion.
        Ejemplo
        let contador = 0;
        do {
            console.log("contador = " + contador);
            contador++
            }while (contador<=5);
        </p>

        <h3>¿Que es un ciclo infinito y por que es un problema?</h3>
        <p>cuando la validacion de nuestros condicionales nunca se cumple y termina (dañando) la app </p>

        <h3>¿Puedo mezclar ciclos y condicionales?</h3>
        <p> Si, nos permiten controlar el flujo de un programa y tomar decisiones basadas en ciertas condiciones
            Ejemplo
        de ciclos y condicionales juntos

        for (let i = 0; i < 5; i++){: <!-- Inicializa una variable i con el valor 0. El bucle se ejecutará mientras i sea menor que 5, y en cada iteración, i se incrementará en 1. -->
            if (i == 2) { :<!-- Dentro del bucle, hay una condición que verifica si i es igual a 2. Si esta condición se cumple, se ejecuta la instrucción break, que sale inmediatamente del bucle for. --> 
                break; 
            }
            console.log(Número ${i});:<!--Se imprime en la consola el valor de i en cada iteración del bucle, pero si i es igual a 2, el break evita que se llegue a esta línea. --> 
                }
        </p>
        <h3> Replica el comportamiento de los siguientes ciclos for utilizando el ciclo while

            for (let i = 0; i < 5; i++) {
                console.log("El valor de i es: " + i);
            }
            
            for (let i = 10; i >= 2; i--) {
                console.log("El valor de i es: " + i);
            }
        </h3>

        <p> R//:
        let i = 0; 
        while(i < 5){
            console.log("El valor de i es: "+ i);
            i++;
        } 

        let i = 10;
        while(i >= 2 ){
            console.log("El valor de i es: " + i)
            i--;
        }
        </p>

        <h3>Escriba un codigo de JS que le pregunte al usuario cuanto es 2 + 2. si el responde bien ,
            mostramos un mensaje de felicitaciones, pero si responde mal  volvemos a empezar</h3>
            <p> R//:
                let num = prompt("Cuanto es 2 + 2");
                if (num == 4 ) {
                    alert ("Felicidades!")
                    } else{
                        alert ("Vuelve a intentarlo")
                        }
                        </p>
                       
<h3>¿Que es un array?</h3>
<p>  Es una lista de elementos en posiciones indexadas numéricamente, 
    comenzando desde el índice 0.
Ejemplo
const array = [1,  "Estefania ", true, false];

</p>

    <h3>¿Que es un objeto</h3>
    <p> R//:Es una lista de elementos que almacena pares clave-valor, donde cada clave es única.
        Ejemplo
        
        const miObjeto = { 
            clave1: valor1, 
            Nombre: "Estefania", 
            Edad: 26
            };
        </p>
        
        <h3>¿Cuando es mejor usar objetos o arrays?</h3>
        <p>R//:
        Usar un Array:
        Cuando necesitas una colección ordenada de elementos y la posición relativa de cada elemento es importante (por ejemplo, una lista de tareas, un conjunto de números).
        Cuando los elementos se pueden identificar y manipular fácilmente a través de un índice numérico.
        
        Usar un Objeto:
        Cuando necesitas almacenar información que tiene una relación clave-valor (por ejemplo, detalles de un usuario, configuraciones).
        Cuando la estructura de los datos es más compleja y no se ajusta fácilmente a un índice numérico.
            
        </p>
        <h3>Crea una funcion que pueda recibir cual quier array como parametro e imprima su primer elemento</h3>
       <p>R//:

        function numero(arreglo) {
            if (arreglo.length > 0) {
                console.log(arreglo[0]);
            } else {
                console.log("Arreglo vacío");
            }
        }
        var array = [1, 2, 3, 4, 5];
        numero(array);
       </p>

     <h3>Crea una funcion que pueda recibir cual quier array como parametro e
    imprima rodos sus elementos uno por uno pero no el array completo</h3>

   <p> R//: 

    function imprimirElementos(arreglo) {
        for (let i = 0; i < arreglo.length; i++) {
            console.log(arreglo[i]);
        }
    }
    
    let miArreglo = [1, 2, 3, 4, 5];
    imprimirElementos(miArreglo);
        </p>

        <h3>Crea una funcion que pueda recibir cual quier objeto como parametro e
            imprima rodos sus elementos uno por uno pero no el objeto completo</h3>
            <p>R//:
                function imprimirElementosObjeto(objeto) {
                    for (const clave in objeto) {
                        console.log(clave + ": " + objeto[clave]);
                    }
                }
                const fruta = {
                    tipo: "Manzana",
                    color: "Rojo",
                    sabor: "Dulce"
                };
                imprimirElementosObjeto(fruta);
            </p>





                 
    </body>
    </html>