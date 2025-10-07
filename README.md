<div align="center">

![Universidad Peruana de Ciencias Aplicadas](https://static.wikia.nocookie.net/logopedia/images/2/2d/UPC-Logo-Actual.png/revision/latest/scale-to-width-down/384?cb=20230305155749&path-prefix=es)

</div>


# **1. Introduccion**

# **2. Integrantes**

  <table border="1px" align="center">
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Código</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Antonio Francisco Datto Aponte</td>
            <td>u202017033</td>
        </tr>
        <tr>
            <td>Edison Jean Franco Coaguila Fuentes</td>
            <td>u202213102</td>
        </tr>
        <tr>
            <td>Luis Enrique Zegarra Garcia</td>
            <td>u202123273</td>
        </tr>
        <tr>
            <td>Joe Maicol Turpo Queque</td>
            <td>u202124254</td>
        </tr>
    </tbody>
</table>


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