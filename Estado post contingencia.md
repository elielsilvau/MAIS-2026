# NTSyCS 2026: A saber

### Tipos de contingencias

- <u>Contingencia simple</u>: Falla o desconexión intempestiva `de un elemento` del SI, pudiendo ser una unidad **generadora**, un **Elemento serie** del ST, una **Barra de consumo**, un **Elemento paralelo** del ST, entre otros, y que `no se propaga a otras instalaciones` del SI.  
En el caso de centrales de ciclo combinado con configuración TG-TV (1:1), corresponde a la desconexión de ambas unidades. En el caso de centrales de ciclo combinado con configuración 2:1, corresponde a la desconexión de una TG y a la pérdida de la generación de la TV sólo en la proporción correspondiente.

- <u>Contingencia crítica</u>: Falla o desconexión intempestiva de `una o más instalaciones` y que no puede ser controlada mediante los Recursos Generales de Control de Contingencias, `debiéndose aplicar Recursos Adicionales de Control de Contingencias` para evitar un Apagón Parcial.

- <u>Contingencia extrema</u>: Falla que `afecta una o más instalaciones` y que no puede ser controlada mediante los Recursos Generales de Control de Contingencias, debiéndose aplicar Recursos Adicionales de Control de Contingencias para evitar un Apagón Total.
Se entiende que la contingencia no puede ser controlada cuando ésta se propaga a las restantes instalaciones del SI, `produciéndose la salida en cascada de otros componentes` debido a sobrecargas inadmisibles, o a pérdida de estabilidad de frecuencia, ángulo y/o tensión.
A los efectos de la presente NT, son fallas de baja probabilidad de ocurrencia:
    - las fallas o desconexiones intempestivas de transformadores de poder o secciones de barras (severidades 8 y 9)
    - la falla que provoca **apertura simultánea de ambos circuitos de una línea de doble circuito** (severidad 6)
    - la falla de un Elemento Serie seguida de la operación errónea del Sistema de Protecciones en un extremo, debiendo operar las Protecciones de Respaldo Local o Remoto (severidad 7).

### Estados de operación

- <u>Estado de alerta</u>: Estado que se alcanza `luego de una o más contingencias, encontrándose el SI previamente en Estado Normal`, en el cual:
    - **no existe** Energía No Suministrada;
    - el SI puede superar **sin pérdida de sincronismo** una nueva contingencia simple de severidad 2;
    - el SI se encuentra operando en forma estable **sin estar disgregado en islas**;
    - y adicionalmente se cumple al menos una de las dos condiciones siguientes:
        - Existen barras del SI cuyas tensiones se encuentran **fuera de los rangos de Estado Normal**, pero **no se encuentran fuera de los rangos de Estado de Alerta**.
        - Se ha perdido reserva en giro de modo que frente a cambios en la demanda, la frecuencia del SI excursiona **fuera de los rangos de Estado Normal**, pero **no fuera de los rangos de Estado de Alerta**.

- <u>Estado de Emergencia</u>: Estado que se alcanza `luego de una o más contingencias encontrándose el SI previamente en Estado Normal o en Estado de Alerta` y en el cual se presentan alguna de las siguientes condiciones:
    - El SI se encuentra **disgregado en Islas** o **existe Energía No Suministrada**.
    - Existen barras del SI cuyas **tensiones se encuentran fuera de los rangos de Estado Normal y Alerta**.
    - Se ha perdido la reserva en giro de modo que frente a cambios en la demanda la **frecuencia del sistema excursiona fuera de los rangos de Estado Normal y Alerta**, con riesgo de que el SI o algunas islas pierdan sincronismo.

- <u>Estado normal</u>: Estado del SI en que se satisfacen simultáneamente las siguientes condiciones:
    - **No existe Energía No Suministrada**.
    - Las **tensiones** en todas las barras del SI se encuentran **dentro de los rangos** definidos **para Estado Normal**.
    - La **frecuencia** se encuentra **dentro del rango definido para Estado Normal**.
    - Las reservas de potencia en giro y de capacidad de transmisión y aporte de reactivos están dentro de los valores programados.
    - El SI puede superar sin pérdida de sincronismo una de las contingencias establecidas en el Artículo 5-31.

### Severidad de contingencias

- <u>Severidad 1</u>: Desconexión intempestiva de un condensador serie.
- <u>Severidad 2</u>: Cortocircuito monofásico sin impedancia de falla en un circuito de líneas de transmisión de doble circuito o en una línea de simple circuito, con o sin Enmallamiento, seguido de la apertura en tiempo normal de la fase fallada por acción de su Sistema de Protecciones y posterior reconexión monofásica exitosa; o, falla de un polo de un enlace HVDC con re-encendido exitoso.
- <u>Severidad 3</u>: Cortocircuito bifásico a tierra sin impedancia de falla en una línea de simple circuito sin Enmallamiento, seguido de la desconexión de la línea en tiempo normal por acción de su Sistema de Protecciones.
- <u>Severidad 4</u>: Cortocircuito bifásico a tierra sin impedancia de falla en un circuito de líneas de doble circuito, o en una línea de simple circuito con Enmallamiento, seguido de la desconexión en tiempo normal del circuito fallado por acción de su Sistema de Protecciones; o, falla permanente de un polo de un enlace HVDC de más de un polo.
- <u>Severidad 5</u>: Desconexión intempestiva de la unidad generadora o del Sistema de Almacenamiento de Energía de mayor tamaño. En el caso de centrales de ciclo combinado deberá considerarse la configuración turbina de gas – turbina de vapor para determinar si la contingencia simple pudiera afectar total o parcialmente a más de una unidad generadora; o, desconexión intempestiva de un Elemento Serie del ST que implique la salida de servicio de más de una unidad generadora; o, la desconexión intempestiva del mayor bloque de demanda en distintas zonas del SI que pueda presentarse como resultado de una Contingencia Simple en las Instalaciones de Clientes; o, una falla permanente en el polo de un enlace HVDC monopolar.
- <u>Severidad 6</u>: Cortocircuito bifásico a tierra sin impedancia de falla en uno de los circuitos de líneas de doble circuito, seguido de la desconexión en tiempo normal del circuito fallado por acción de su sistema de protecciones y la salida intempestiva simultánea del circuito sano en paralelo por actuación errónea de los Sistemas de Protecciones de este último; o falla permanente de todos los polos de un enlace HVDC de más de un polo.
- <u>Severidad 7</u>: Cortocircuito bifásico a tierra sin impedancia de falla en una línea de simple circuito con Enmallamiento o en uno de los circuitos de líneas de doble circuito, seguido de la falla en la operación de su Sistema de Protecciones en un extremo del circuito, lo que produce el despeje de la falla por acción normal de la Protección de Respaldo Local o Remoto.
- <u>Severidad 8</u>: Desconexión intempestiva de un transformador de poder.
- <u>Severidad 9</u>: Cortocircuito monofásico a tierra sin impedancia de falla de una sección de barra de una subestación, seguido de su desconexión en tiempo normal por acción de los Sistemas de Protecciones que cubren la barra