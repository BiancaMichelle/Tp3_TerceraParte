# Tp3_TerceraParte
### 1- Patrón Builder


![Captura](https://github.com/user-attachments/assets/27d26d29-999d-4aed-9413-07160d8e40e8)


El diagrama de clases representa el diseño de un sistema de gestión de reservas de vuelo. Se utilizó el patrón de diseño Builder para impletar un constructor el cuál arma las distintas reservas de vuelo con características específicas.


### 2- Patrón Factory Method

![Diagrama de Clase - Gestor de Pagos](https://github.com/user-attachments/assets/4f61c129-81ee-4d51-8287-6ed9ba66abf1)

El diagrama de clases de la parte superior representa un sistema de gestión de pagos con la implementación y utilización del patrón de diseño creacional "Factory Method", este mismo resulta útil dado a que separa el código de construcción del código que hace uso del objeto. Por ello, es más fácil extender el código de construcción de forma independiente al resto del código. Además, este método trae la ventaja de permitirnos ahorrar recursos al reutilizar objetos ya construidos antes que estarlos construyendo una y otra vez.

### 3- Patrón Singleton


![image](https://github.com/user-attachments/assets/2421f4f3-bc00-4dda-abd4-a064d3cccb67)

El diagrama de clases representa el diseño de un sistema de logging basado en el patrón Singleton. La clase Logger se marca con el estereotipo <Singleton>, lo que indica que solo debe existir una única instancia de esta clase en todo el sistema, cumpliendo con el patrón Singleton. Este patrón se refuerza con el atributo estático instance: Logger y el método getInstance(): Logger, que proporciona acceso a la única instancia de Logger y garantiza que el registro de logs se gestione desde un punto centralizado.

La relación de dependencia entre LoggingSimulador y Logger, representada por la flecha etiquetada como "Ejecuta", muestra que LoggingSimulador usa la instancia única de Logger para registrar mensajes. En el método run(), LoggingSimulador envía mensajes simulados de distintos tipos (información, advertencia, error) a Logger, reflejando su función como un generador de logs en un contexto de simulación.

La asociación entre Cliente y Logger, etiquetada como "accede", indica que Cliente también utiliza la instancia única de Logger para registrar eventos. La multiplicidad 1 en ambos extremos de la relación muestra que cada Cliente accede a la misma instancia de Logger, en línea con el diseño Singleton que proporciona un recurso compartido centralizado.

Dentro de Logger, los métodos logInfo, logWarning, logError, y log representan la funcionalidad de registro en distintos niveles de severidad. Estos métodos permiten registrar mensajes variados, mientras que el método privado log(String message) maneja la lógica interna para escribir el mensaje en un archivo. Esto encapsula la funcionalidad de Logger y asegura una interfaz clara y organizada para el registro de logs.
