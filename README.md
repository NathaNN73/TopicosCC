# **1. Introduccion**

# **2. Integrantes**

# **3. Problema elegido**

# **4. Solucion**
## **4.1 Breve explicacion de la solucion**

El problema se modela utilizando el solver de OrTools con el objetivo de encontrar un emparejamiento entre 6 hombres y 6 mujeres que sea estable, es decir, donde no existan dos parejas que prefieran estar juntas antes que con sus parejas actuales. Además, se impone la restricción adicional de que cada mujer debe estar emparejada con un hombre que se encuentre como máximo en su 4ta preferencia. El solver buscará todas las soluciones posibles que cumplan estas condiciones.

## **4.2 Variables**

Se definieron los siguientes elementos en la solución:

- Matrices de preferencias:

    - tablero_m: Matriz numérica que almacena las preferencias de los hombres sobre las mujeres (donde un número menor indica mayor preferencia).

    - tablero_w: Matriz numérica que almacena las preferencias de las mujeres sobre los hombres (misma convención).

- Modelo CSP:

    - model: Instancia de cp_model.CpModel() que contiene la definición del problema, incluyendo variables y restricciones.

    - Variables de decisión:

        - parejas: Matriz booleana de 6x6, donde parejas[m][w] es una variable binaria que indica si el hombre m está emparejado con la mujer w (True) o no (False). Estas son las variables principales que el solver debe determinar.

- Solver:

    - solver: Instancia de CpSolver() utilizada para resolver el modelo y encontrar las soluciones factibles.

## **4.3 Reestricciones**

## **4.4 Resultados**

# **4.5 Conclusiones**