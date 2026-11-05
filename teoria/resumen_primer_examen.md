#Tema 1. Definiciones

##**Que es un sistema operativo'**
No existe una definicion universal de sistema operativo; se define mejor por lo que hace que por lo que es
La definicion "El programa que se ejecuta constantemente en el ordenador": en realidad lo que se ejecuta continuamente es el kernel o nucleo. Falla porque:
- Excluye servicios que intuitivamente son parte del SO
- En los microkernels (funcionalidad minima en el nucleo) dejaria fuera cosas como red, archivos o memoria virtual.
En la perspectiva comercial es SO lo que te venden cuando compras un ordenador. Tampoco precisa (desde 1MB sin aplicaciones hasta GBs con GUI y aplicaciones)

##El sistema informatico consta de 4 componente
1. Hardware (CPU, memoria, E/S): recursos computacionales
2. Programas de aplicacion: resuelven problemas de los usuarios
3. Usuarios
4. Sistema opetarivo: controla, coordina el acceso y asigna recursos

##Funciones del SO
Se dividen en dos:
Perspectiva del sistema informatico:
- Gestiona los recursos computacionales (hardware y software) del sistema
- Controla la ejecucion de los programas de usuario y el acceso a los dispositivos de E/S
- Resuelve conflictos en las peticiones y previene errores y usos inadecuados
- El SO no hace trabajo util directamente: proporciona un entorno para que lo hagan las aplicaciones

Persepectiva del usuario (varia segun el sistema, poco precisa);
- Interfaz de usuario (GUI o linea de comandos)
- Organizacion y gestion del almacenamiento (directorios, copiar, borrar, proteger...)
- Ejecucion de programas (iniciar, detener, multitarea...)

En escritorio, mainframe y sistemas empotrados el SO siempre tiene las mismas funciones; lo que cambia es como las implementa segun los objetivos del diseño
| :Escritorio:| :Facilidad de uso: |
| :Mainframe: | :Aprovechamiento de recursos: |
| :Sistemas empotrados: | :Fiabilidad: |

#Tema 2. Tipos de sistemas operativos

##Mainframe
No se caracterizan tanto por la potencia de CPU sino por la gran memoria, gran almacenamiento, E/S rapida y alta fiabilidad.

Evolucion:
| Sistema | Idea | Problema que resuelven/presenta |
| Proceso por lotes (batch) | El monitor del sistema carga y ejecuta un lote de programas uno tras otro automaticamente | La CPU queda inutil durante la E/S |
| Multiprgramados | Varios programas en memoria, ejecucion intercalada | Sigue sin interactuar con el usuario |
| Tiempo compartido | Terminales + cuanto o ventana de tiempo de CPU por usuario | Complejidad: memoria virtual, sincronizacion, archivos |

##Monitor del sistema (predecesor del SO):
- Permanece siempre cargadi en memoria
- Su única tarea: pasar automaticamente de un programa al siguiente
- Ejecuta un solo programa a la vez. la CPU se sigue quedando inutil mientras E/S

##Sistemas multiprogamados:
- Varios trabajos en memoria a la vez (grado de multiprogramacion = numero de programas cargados en memoria en un instante)
- Al pedir un trabajo la E/S, el SO lo suspende y da la CPU a otro
- Cuando termina la E/S de un trabajo suspendido, NO interrumpe al que ocupa la CPU, espera a que este termine o pida E/S
- Tres tareas esenciales del SO: Planificacion de trabajos (que cargar en memoria) , planificacion de la CPU (que ejecutar) y gestion de la memoria.

 

