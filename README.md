# Taller Nro 2 Bases de datos

1. ```sql
   SELECT apellido1 FROM empleado; 
   ```

   ```
   +-----------+
   | apellido1 |
   +-----------+
   | Rivero    |
   | Salas     |
   | Rubio     |
   | Suárez    |
   | Loyola    |
   | Santana   |
   | Ruiz      |
   | Ruiz      |
   | Gómez     |
   | Flores    |
   | Herrera   |
   | Salas     |
   | Sáez      |
   +-----------+
   ```

2. ```sql
   SELECT DISTINCT apellido1 FROM empleado; 
   ```

   ```
   +-----------+
   | apellido1 |
   +-----------+
   | Rivero    |
   | Salas     |
   | Rubio     |
   | Suárez    |
   | Loyola    |
   | Santana   |
   | Ruiz      |
   | Gómez     |
   | Flores    |
   | Herrera   |
   | Sáez      |
   +-----------+
   ```

3. ```sql
   SELECT  codigo, nif,nombre, apellido1,apellido2, codigo_departamento FROM empleado;  
   ```

   ```
   +--------+-----------+--------------+-----------+-----------+---------------------+
   | codigo | nif       | nombre       | apellido1 | apellido2 | codigo_departamento |
   +--------+-----------+--------------+-----------+-----------+---------------------+
   |      1 | 32481596F | Aarón        | Rivero    | Gómez     |                   1 |
   |      2 | Y5575632D | Adela        | Salas     | Díaz      |                   2 |
   |      3 | R6970642B | Adolfo       | Rubio     | Flores    |                   3 |
   |      4 | 77705545E | Adrián       | Suárez    | NULL      |                   4 |
   |      5 | 17087203C | Marcos       | Loyola    | Méndez    |                   5 |
   |      6 | 38382980M | María        | Santana   | Moreno    |                   1 |
   |      7 | 80576669X | Pilar        | Ruiz      | NULL      |                   2 |
   |      8 | 716514317 | Pepe         | Ruiz      | Santana   |                   3 |
   |      9 | 56399183D | Juan         | Gómez     | López     |                   2 |
   |     10 | 46384486H | Diego        | Flores    | Salas     |                   5 |
   |     11 | 67389283A | Marta        | Herrera   | Gil       |                   1 |
   |     12 | 41234836R | Irene        | Salas     | Flores    |                NULL |
   |     13 | 82635162B | Juan Antonio | Sáez      | Guerrero  |                NULL |
   +--------+-----------+--------------+-----------+-----------+---------------------+
   ```

4. ```sql
   SELECT  nombre, apellido1,apellido2 FROM empleado; 
   ```

   ```
   +--------------+-----------+-----------+
   | nombre       | apellido1 | apellido2 |
   +--------------+-----------+-----------+
   | Aarón        | Rivero    | Gómez     |
   | Adela        | Salas     | Díaz      |
   | Adolfo       | Rubio     | Flores    |
   | Adrián       | Suárez    | NULL      |
   | Marcos       | Loyola    | Méndez    |
   | María        | Santana   | Moreno    |
   | Pilar        | Ruiz      | NULL      |
   | Pepe         | Ruiz      | Santana   |
   | Juan         | Gómez     | López     |
   | Diego        | Flores    | Salas     |
   | Marta        | Herrera   | Gil       |
   | Irene        | Salas     | Flores    |
   | Juan Antonio | Sáez      | Guerrero  |
   +--------------+-----------+-----------+
   ```

5. ```sql
   SELECT codigo_departamento FROM empleado; 
   ```

   ```
   +---------------------+
   | codigo_departamento |
   +---------------------+
   |                NULL |
   |                NULL |
   |                   1 |
   |                   1 |
   |                   1 |
   |                   2 |
   |                   2 |
   |                   2 |
   |                   3 |
   |                   3 |
   |                   4 |
   |                   5 |
   |                   5 |
   +---------------------+
   ```

6. ```sql
   SELECT DISTINCT codigo_departamento FROM empleado; 
   ```

   ```
   +---------------------+
   | codigo_departamento |
   +---------------------+
   |                NULL |
   |                   1 |
   |                   2 |
   |                   3 |
   |                   4 |
   |                   5 |
   +---------------------+
   ```

7. ```sql
   SELECT CONCAT(nombre, ' ', apellido1, ' ', apellido2) AS nombre_completo
   FROM empleado;
   ```

```
+-----------------------------+
| nombre_completo             |
+-----------------------------+
| Aarón Rivero Gómez          |
| Adela Salas Díaz            |
| Adolfo Rubio Flores         |
| NULL                        |
| Marcos Loyola Méndez        |
| María Santana Moreno        |
| NULL                        |
| Pepe Ruiz Santana           |
| Juan Gómez López            |
| Diego Flores Salas          |
| Marta Herrera Gil           |
| Irene Salas Flores          |
| Juan Antonio Sáez Guerrero  |
+-----------------------------+
```

8. ```sql
   SELECT UPPER(CONCAT(nombre, ' ', apellido1, ' ', apellido2)) AS nombre_completo_upper
   FROM empleado;
   ```

   ```
   +-----------------------------+
   | nombre_completo_upper       |
   +-----------------------------+
   | AARÓN RIVERO GÓMEZ          |
   | ADELA SALAS DÍAZ            |
   | ADOLFO RUBIO FLORES         |
   | NULL                        |
   | MARCOS LOYOLA MÉNDEZ        |
   | MARÍA SANTANA MORENO        |
   | NULL                        |
   | PEPE RUIZ SANTANA           |
   | JUAN GÓMEZ LÓPEZ            |
   | DIEGO FLORES SALAS          |
   | MARTA HERRERA GIL           |
   | IRENE SALAS FLORES          |
   | JUAN ANTONIO SÁEZ GUERRERO  |
   +-----------------------------+
   ```

9. ```sql
   SELECT LOWER(CONCAT(nombre, ' ', apellido1, ' ', apellido2)) AS nombre_completo_upper
   FROM empleado;
   ```

   ```
   +-----------------------------+
   | nombre_completo_upper       |
   +-----------------------------+
   | aarón rivero gómez          |
   | adela salas díaz            |
   | adolfo rubio flores         |
   | NULL                        |
   | marcos loyola méndez        |
   | maría santana moreno        |
   | NULL                        |
   | pepe ruiz santana           |
   | juan gómez lópez            |
   | diego flores salas          |
   | marta herrera gil           |
   | irene salas flores          |
   | juan antonio sáez guerrero  |
   +-----------------------------+
   ```

10. ```sql
    SELECT id_empleado,
           SUBSTRING(nif, 1, LENGTH(nif) - 1) AS nif_digitos,
           RIGHT(nif, 1) AS nif_letra
    FROM empleados;
    ```

    ```
    +--------+-------------+-----------+
    | codigo | nif_digitos | nif_letra |
    +--------+-------------+-----------+
    |      1 | 32481596    | F         |
    |      2 | Y5575632    | D         |
    |      3 | R6970642    | B         |
    |      4 | 77705545    | E         |
    |      5 | 17087203    | C         |
    |      6 | 38382980    | M         |
    |      7 | 80576669    | X         |
    |      8 | 71651431    | Z         |
    |      9 | 56399183    | D         |
    |     10 | 46384486    | H         |
    |     11 | 67389283    | A         |
    |     12 | 41234836    | R         |
    |     13 | 82635162    | B         |
    +--------+-------------+-----------+
    ```

11. ```sql
    SELECT nombre,
           presupuesto - gastos AS presupuesto_actual
    FROM departamento;
    ```

    ```
    +------------------+--------------------+
    | nombre           | presupuesto_actual |
    +------------------+--------------------+
    | Desarrollo       |             114000 |
    | Sistemas         |             129000 |
    | Recursos Humanos |             255000 |
    | Contabilidad     |             107000 |
    | I+D              |              -5000 |
    | Proyectos        |                  0 |
    | Publicidad       |              -1000 |
    +------------------+--------------------+
    ```

12. ```sql
    SELECT nombre,
           presupuesto - gastos AS presupuesto_actual
    FROM departamento
    ORDER BY presupuesto_actual ASC;
    ```

    ```
    +------------------+--------------------+
    | nombre           | presupuesto_actual |
    +------------------+--------------------+
    | I+D              |              -5000 |
    | Publicidad       |              -1000 |
    | Proyectos        |                  0 |
    | Contabilidad     |             107000 |
    | Desarrollo       |             114000 |
    | Sistemas         |             129000 |
    | Recursos Humanos |             255000 |
    +------------------+--------------------+
    ```

13. ```sql
    SELECT nombre
    FROM departamento
    ORDER BY nombre ASC;
    ```

    ```
    +------------------+
    | nombre           |
    +------------------+
    | Contabilidad     |
    | Desarrollo       |
    | I+D              |
    | Proyectos        |
    | Publicidad       |
    | Recursos Humanos |
    | Sistemas         |
    +------------------+
    ```

14. ```sql
    SELECT nombre
    FROM departamento
    ORDER BY nombre DESC;
    ```

    ```
    +------------------+
    | nombre           |
    +------------------+
    | Sistemas         |
    | Recursos Humanos |
    | Publicidad       |
    | Proyectos        |
    | I+D              |
    | Desarrollo       |
    | Contabilidad     |
    +------------------+
    ```

15. ```sql
    SELECT apellido1, apellido2, nombre
    FROM empleado
    ORDER BY apellido1 ASC, nombre ASC;
    ```

    

    ```
    +-----------+-----------+--------------+
    | apellido1 | apellido2 | nombre       |
    +-----------+-----------+--------------+
    | Flores    | Salas     | Diego        |
    | Gómez     | López     | Juan         |
    | Herrera   | Gil       | Marta        |
    | Loyola    | Méndez    | Marcos       |
    | Rivero    | Gómez     | Aarón        |
    | Rubio     | Flores    | Adolfo       |
    | Ruiz      | Santana   | Pepe         |
    | Ruiz      | NULL      | Pilar        |
    | Sáez      | Guerrero  | Juan Antonio |
    | Salas     | Díaz      | Adela        |
    | Salas     | Flores    | Irene        |
    | Santana   | Moreno    | María        |
    | Suárez    | NULL      | Adrián       |
    +-----------+-----------+--------------+
    ```

16. ```sql
    SELECT nombre, presupuesto
    FROM departamento
    ORDER BY presupuesto DESC
    LIMIT 3;
    ```

    ```
    +------------------+-------------+
    | nombre           | presupuesto |
    +------------------+-------------+
    | I+D              |      375000 |
    | Recursos Humanos |      280000 |
    | Sistemas         |      150000 |
    +------------------+-------------+
    ```

17. ```sql
    SELECT nombre, presupuesto
    FROM departamento
    ORDER BY presupuesto ASC
    LIMIT 3;
    ```

    ```
    +--------------+-------------+
    | nombre       | presupuesto |
    +--------------+-------------+
    | Proyectos    |           0 |
    | Publicidad   |           0 |
    | Contabilidad |      110000 |
    +--------------+-------------+
    ```

18. ```sql
    SELECT nombre, gastos
    FROM departamento
    ORDER BY gastos DESC
    LIMIT 2;
    ```

    ```
    +------------------+--------+
    | nombre           | gasto |
    +------------------+--------+
    | I+D              | 380000 |
    | Recursos Humanos |  25000 |
    +------------------+--------+
    ```

19. ```sql
    SELECT nombre, gasto
    FROM departamento
    ORDER BY gasto ASC
    LIMIT 2;
    ```

    ```
    +------------+-------+
    | nombre     | gasto |
    +------------+-------+
    | Proyectos  |     0 |
    | Publicidad |  1000 |
    +------------+-------+
    ```

20. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    LIMIT 5 OFFSET 2;
    ```

    ```
    +--------+-----------+---------+-----------+-----------+------------+
    | codigo | nif       | nombre  | apellido1 | apellido2 | cod_depart |
    +--------+-----------+---------+-----------+-----------+------------+     |      3 | R6970642B | Adolfo  | Rubio     | Flores    |          3 |
    |      4 | 77705545E | Adrián  | Suárez    | NULL      |          4 |
    |      5 | 17087203C | Marcos  | Loyola    | Méndez    |          5 |
    |      6 | 38382980M | María   | Santana   | Moreno    |          1 |
    |      7 | 80576669X | Pilar   | Ruiz      | NULL      |          2 |
    +--------+-----------+---------+-----------+-----------+------------+
    ```

21. ```sql
    SELECT nombre, presupuesto
    FROM departamento
    WHERE presupuesto >= 150000;
    ```

    ```
    +------------------+-------------+
    | nombre           | presupuesto |
    +------------------+-------------+
    | Sistemas         |      150000 |
    | Recursos Humanos |      280000 |
    | I+D              |      375000 |
    +------------------+-------------+
    ```

22. ```sql
    SELECT nombre, gasto
    FROM departamento
    WHERE gasto < 5000;
    ```

    ```
    +--------------+-------+
    | nombre       | gasto |
    +--------------+-------+
    | Contabilidad |  3000 |
    | Proyectos    |     0 |
    | Publicidad   |  1000 |
    +--------------+-------+
    ```

23. ```sql
    SELECT nombre, presupuesto
    FROM departamento
    WHERE presupuesto >= 100000 AND presupuesto <= 200000;
    ```

    ```
    +--------------+-------------+
    | nombre       | presupuesto |
    +--------------+-------------+
    | Desarrollo   |      120000 |
    | Sistemas     |      150000 |
    | Contabilidad |      110000 |
    +--------------+-------------+
    ```

24. ```sql
    SELECT nombre
    FROM departamento
    WHERE presupuesto < 100000 OR presupuesto > 200000;
    ```

    ```
    +------------------+
    | nombre           |
    +------------------+
    | Recursos Humanos |
    | I+D              |
    | Proyectos        |
    | Publicidad       |
    +------------------+
    ```

25. ```sql
    SELECT nombre
    FROM departamento
    WHERE presupuesto BETWEEN 100000 AND 200000;
    ```

    ```
    +--------------+
    | nombre       |
    +--------------+
    | Desarrollo   |
    | Sistemas     |
    | Contabilidad |
    +--------------+
    ```

26. ```sql
    SELECT nombre
    FROM departamento
    WHERE presupuesto NOT BETWEEN 100000 AND 200000;
    ```

    ```
    +------------------+
    | nombre           |
    +------------------+
    | Recursos Humanos |
    | I+D              |
    | Proyectos        |
    | Publicidad       |
    +------------------+
    ```

27. ```sql
    SELECT nombre, gasto, presupuesto
    FROM departamento
    WHERE gasto > presupuesto;
    ```

    ```
    +------------+--------+-------------+
    | nombre     | gasto  | presupuesto |
    +------------+--------+-------------+
    | I+D        | 380000 |      375000 |
    | Publicidad |   1000 |           0 |
    +------------+--------+-------------+
    ```

28. ```sql
    SELECT nombre, gasto, presupuesto
    FROM departamento
    WHERE gasto < presupuesto;
    ```

    ```
    +------------------+-------+-------------+
    | nombre           | gasto | presupuesto |
    +------------------+-------+-------------+
    | Desarrollo       |  6000 |      120000 |
    | Sistemas         | 21000 |      150000 |
    | Recursos Humanos | 25000 |      280000 |
    | Contabilidad     |  3000 |      110000 |
    +------------------+-------+-------------+
    ```

29. ```sql
    SELECT nombre, gasto, presupuesto
    FROM departamento
    WHERE gasto = presupuesto;
    ```

    ```
    +-----------+-------+-------------+
    | nombre    | gasto | presupuesto |
    +-----------+-------+-------------+
    | Proyectos |     0 |           0 |
    +-----------+-------+-------------+
    ```

30. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    WHERE apellido2 IS NULL;
    ```

    ```
    +--------+-----------+---------+-----------+-----------+---------------+
    | codigo | nif       | nombre  | apellido1 | apellido2 | codigo_depart |
    +--------+-----------+---------+-----------+-----------+---------------+
    |      4 | 77705545E | Adrián  | Suárez    | NULL      |             4 |
    |      7 | 80576669X | Pilar   | Ruiz      | NULL      |             2 |
    +--------+-----------+---------+-----------+-----------+---------------+
    ```

31. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    WHERE apellido2 IS NOT NULL;
    ```

    ```
    +--------+-----------+--------------+-----------+-----------+------------+
    | codigo | nif       | nombre       | apellido1 | apellido2 | cod_depart |
    +--------+-----------+--------------+-----------+-----------+------------+
    |      1 | 32481596F | Aarón        | Rivero    | Gómez     |          1 |
    |      2 | Y5575632D | Adela        | Salas     | Díaz      |          2 |
    |      3 | R6970642B | Adolfo       | Rubio     | Flores    |          3 |
    |      5 | 17087203C | Marcos       | Loyola    | Méndez    |          5 |
    |      6 | 38382980M | María        | Santana   | Moreno    |          1 |
    |      8 | 71651431Z | Pepe         | Ruiz      | Santana   |          3 |
    |      9 | 56399183D | Juan         | Gómez     | López     |          2 |
    |     10 | 46384486H | Diego        | Flores    | Salas     |          5 |
    |     11 | 67389283A | Marta        | Herrera   | Gil       |          1 |
    |     12 | 41234836R | Irene        | Salas     | Flores    |       NULL |
    |     13 | 82635162B | Juan Antonio | Sáez      | Guerrero  |       NULL |
    +--------+-----------+--------------+-----------+-----------+------------+
    ```

32. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    WHERE apellido2 = 'López';
    ```

    ```
    +--------+-----------+--------+-----------+-----------+---------------+
    | codigo | nif       | nombre | apellido1 | apellido2 | codigo_depart |
    +--------+-----------+--------+-----------+-----------+---------------+
    |      9 | 56399183D | Juan   | Gómez     | López     |             2 |
    +--------+-----------+--------+-----------+-----------+---------------+
    ```

33. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    WHERE apellido2 = 'Díaz' OR apellido2 = 'Moreno';
    ```

    ```
    +--------+-----------+--------+-----------+-----------+---------------+
    | codigo | nif       | nombre | apellido1 | apellido2 | codigo_depart |
    +--------+-----------+--------+-----------+-----------+---------------+
    |      2 | Y5575632D | Adela  | Salas     | Díaz      |             2 |
    |      6 | 38382980M | María  | Santana   | Moreno    |             1 |
    +--------+-----------+--------+-----------+-----------+---------------+
    ```

34. ```sql
    SELECT codigo, nif, nombre, apellido1, apellido2, codigo_departamento
    FROM empleado
    WHERE apellido2 IN ('Díaz', 'Moreno');
    ```

    ```
    +--------+-----------+--------+-----------+-----------+---------------+
    | codigo | nif       | nombre | apellido1 | apellido2 | codigo_depart |
    +--------+-----------+--------+-----------+-----------+---------------+
    |      2 | Y5575632D | Adela  | Salas     | Díaz      |             2 |
    |      6 | 38382980M | María  | Santana   | Moreno    |             1 |
    +--------+-----------+--------+-----------+-----------+---------------+
    ```

35. ```sql
    SELECT e.nombre, e.apellido1, e.apellido2, e.nif
    FROM empleado e
    JOIN departamento d ON e.codigo_departamento = d.codigo
    WHERE d.codigo = 3;
    ```

    ```
    +--------+-----------+-----------+-----------+
    | nombre | apellido1 | apellido2 | nif       |
    +--------+-----------+-----------+-----------+
    | Adolfo | Rubio     | Flores    | R6970642B |
    | Pepe   | Ruiz      | Santana   | 71651431Z |
    +--------+-----------+-----------+-----------+
    ```

36. ```sql
    SELECT nombre, apellido1, apellido2, nif
    FROM empleado
    WHERE codigo_departamento IN (2, 4, 5);
    ```

    ```
    +---------+-----------+-----------+-----------+
    | nombre  | apellido1 | apellido2 | nif       |
    +---------+-----------+-----------+-----------+
    | Adela   | Salas     | Díaz      | Y5575632D |
    | Pilar   | Ruiz      | NULL      | 80576669X |
    | Juan    | Gómez     | López     | 56399183D |
    | Adrián  | Suárez    | NULL      | 77705545E |
    | Marcos  | Loyola    | Méndez    | 17087203C |
    | Diego   | Flores    | Salas     | 46384486H |
    +---------+-----------+-----------+-----------+
    ```

# Consultas mutitabla (Composición interna)

1. ```sql
   SELECT e.codigo, e.nif, e.nombre, e.apellido1, e.apellido2, d.nombre AS nombre_depart, d.presupuesto, d.gasto
   FROM empleado e
   JOIN departamento d ON e.codigo_departamento = d.codigo;
   ```

+-----------+------------------+--------------+---------------+---------------+------------------------------+---------------------+----------+
| codigo | nif                 | nombre  | apellido1 | apellido2 | nombre_depart        | presupuesto  | gasto  |
+-----------+-----------+---------+-----------+--------------+---------------+------------------------------+---------------------+------ ----+
|          1 | 32481596F   | Aarón      | Rivero    | Gómez     | Desarrollo                   |      120000      |   6000 |
|          6 | 38382980M  | María      | Santana | Moreno   | Desarrollo                   |      120000      |   6000 |
|        11 | 67389283A  | Marta      | Herrera  | Gil             | Desarrollo                   |      120000      |   6000 |
|          2 | Y5575632D  | Adela      | Salas       | Díaz          | Sistemas                     |      150000       | 21000 |
|          7 | 80576669X   | Pilar        | Ruiz        | NULL        | Sistemas                     |      150000       | 21000 |
|          9 | 56399183D  | Juan         | Gómez  | López       | Sistemas                     |      150000       |  21000 |
|          3 | R6970642B  | Adolfo     | Rubio     | Flores      | Recursos Humanos   |      280000       |  25000 |
|          8 | 71651431Z  | Pepe        | Ruiz        | Santana  | Recursos Humanos   |      280000       |  25000 |
|          4 | 77705545E  | Adrián     | Suárez   | NULL       | Contabilidad                |      110000       |   3000 |
|          5 | 17087203C  | Marcos   | Loyola    | Méndez  | I+D                                 |    375000       | 380000 |
|        10 | 46384486H | Diego      | Flores     | Salas       | I+D                                  |   375000       | 380000 |
+-----------+------------------+--------------+-------------+--------------+---------------------------------+--------------------+-----------+

2. ```sql
   SELECT e.codigo, e.nif, e.nombre, e.apellido1, e.apellido2, d.nombre, d.presupuesto, d.gasto
   FROM empleado e
   JOIN departamento d ON e.codigo_departamento = d.codigo;
   ORDER BY d.nombre ASC, e.apellido1 ASC, e.apellido2 ASC, e.nombre ASC;
   ```

   ```
   +--------+-----------+---------+-----------+-----------+------------------+-------------+--------+
   | codigo | nif       | nombre  | apellido1 | apellido2 | nombre           | presupuesto | gasto  |
   +--------+-----------+---------+-----------+-----------+------------------+-------------+--------+
   |      1 | 32481596F | Aarón   | Rivero    | Gómez     | Desarrollo       |      120000 |   6000 |
   |      6 | 38382980M | María   | Santana   | Moreno    | Desarrollo       |      120000 |   6000 |
   |     11 | 67389283A | Marta   | Herrera   | Gil       | Desarrollo       |      120000 |   6000 |
   |      2 | Y5575632D | Adela   | Salas     | Díaz      | Sistemas         |      150000 |  21000 |
   |      7 | 80576669X | Pilar   | Ruiz      | NULL      | Sistemas         |      150000 |  21000 |
   |      9 | 56399183D | Juan    | Gómez     | López     | Sistemas         |      150000 |  21000 |
   |      3 | R6970642B | Adolfo  | Rubio     | Flores    | Recursos Humanos |      280000 |  25000 |
   |      8 | 71651431Z | Pepe    | Ruiz      | Santana   | Recursos Humanos |      280000 |  25000 |
   |      4 | 77705545E | Adrián  | Suárez    | NULL      | Contabilidad     |      110000 |   3000 |
   |      5 | 17087203C | Marcos  | Loyola    | Méndez    | I+D              |      375000 | 380000 |
   |     10 | 46384486H | Diego   | Flores    | Salas     | I+D              |      375000 | 380000 |
   +--------+-----------+---------+-----------+-----------+------------------+-------------+--------+
   ```

3. ```sql
   SELECT d.codigo, d.nombre
   FROM departamento AS d
   LEFT JOIN empleado AS e ON d.codigo = e.codigo_departamento
   WHERE e.codigo_departamento IS NULL;
   ```

   ```
   +--------+------------+
   | codigo | nombre     |
   +--------+------------+
   |      6 | Proyectos  |
   |      7 | Publicidad |
   +--------+------------+
   ```

4. ```sql
   SELECT d.codigo, d.nombre, (d.presupuesto - d.gasto) AS presupuesto_actual
   FROM departamento AS d
   LEFT JOIN empleado AS e ON d.codigo = e.codigo_departamento
   WHERE e.codigo_departamento IS NOT NULL;
   ```

   ```
   +--------+------------------+--------------------+
   | codigo | nombre           | presupuesto_actual |
   +--------+------------------+--------------------+
   |      1 | Desarrollo       |             114000 |
   |      1 | Desarrollo       |             114000 |
   |      1 | Desarrollo       |             114000 |
   |      2 | Sistemas         |             129000 |
   |      2 | Sistemas         |             129000 |
   |      2 | Sistemas         |             129000 |
   |      3 | Recursos Humanos |             255000 |
   |      3 | Recursos Humanos |             255000 |
   |      4 | Contabilidad     |             107000 |
   |      5 | I+D              |              -5000 |
   |      5 | I+D              |              -5000 |
   +--------+------------------+--------------------+
   ```

5. ```sql
   SELECT d.nombre AS nombre_departamento
   FROM empleado AS e
   JOIN departamento AS d ON e.codigo_departamento = d.codigo
   WHERE e.nif = '38382980M';
   ```

   ```
   +---------------------+
   | nombre_departamento |
   +---------------------+
   | Desarrollo          |
   +---------------------+
   ```

6. ```sql
   SELECT d.nombre AS nombre_departamento
   FROM empleado AS e
   JOIN departamento AS d ON e.codigo_departamento = d.codigo
   WHERE e.nombre = 'Pepe' AND e.apellido1 = 'Ruiz' AND e.apellido2 = 'Santana';
   ```

   ```
   +---------------------+
   | nombre_departamento |
   +---------------------+
   | Recursos Humanos    |
   +---------------------+
   ```

7. ```sql
   SELECT e.nombre, e.apellido1, e.apellido2, e.nif
   FROM empleado AS e
   JOIN departamento AS d ON e.codigo_departamento = d.codigo
   WHERE d.nombre = 'I+D'
   ORDER BY e.nombre ASC;
   ```

   ```
   +--------+-----------+-----------+-----------+
   | nombre | apellido1 | apellido2 | nif       |
   +--------+-----------+-----------+-----------+
   | Marcos | Loyola    | Méndez    | 17087203C |
   | Diego  | Flores    | Salas     | 46384486H |
   +--------+-----------+-----------+-----------+
   ```

8. ```sql
   SELECT e.nombre, e.apellido1, e.apellido2, e.nif
   FROM empleado AS e
   JOIN departamento AS d ON e.codigo_departamento = d.codigo
   WHERE d.nombre = 'I+D' OR d.nombre = 'Sistemas' OR d.nombre = 'Contabilidad' 
   ORDER BY e.nombre ASC;
   ```

   ```
   +---------+-----------+-----------+-----------+
   | nombre  | apellido1 | apellido2 | nif       |
   +---------+-----------+-----------+-----------+
   | Adela   | Salas     | Díaz      | Y5575632D |
   | Adrián  | Suárez    | NULL      | 77705545E |
   | Diego   | Flores    | Salas     | 46384486H |
   | Juan    | Gómez     | López     | 56399183D |
   | Marcos  | Loyola    | Méndez    | 17087203C |
   | Pilar   | Ruiz      | NULL      | 80576669X |
   +---------+-----------+-----------+-----------+
   ```

9. ```sql
   SELECT e.nombre
   FROM empleado AS e
   JOIN departamento AS d ON e.codigo_departamento = d.codigo
   WHERE d.presupuesto < 100000 OR d.presupuesto>200000;
   ```

   ```
   +--------+
   | nombre |
   +--------+
   | Adolfo |
   | Pepe   |
   | Marcos |
   | Diego  |
   +--------+
   ```

10. ```sql
    SELECT d.nombre
    FROM departamento AS d
    JOIN empleado AS e ON d.codigo = e.codigo_departamento
    WHERE e.apellido2 IS NULL;
    ```

    ```
    +--------------+
    | nombre       |
    +--------------+
    | Contabilidad |
    | Sistemas     |
    +--------------+
    ```



# Consultas multitabla (Composición externa)

1. ```sql
   SELECT e.codigo, e.nif, e.nombre AS nombre_empleado, e.apellido1, e.apellido2, 
          d.nombre AS nombre_depart, d.presupuesto, d.gasto
   FROM empleado AS e
   LEFT JOIN departamento AS d ON e.codigo_departamento = d.codigo
   ORDER BY e.nombre, e.apellido1, e.apellido2;
   ```

   ```
   +--------+-----------+-----------------+-----------+-----------+------------------+-------------+--------+
   | codigo | nif       | nombre_empleado | apellido1 | apellido2 | nombre_depart    | presupuesto | gasto  |
   +--------+-----------+-----------------+-----------+-----------+------------------+-------------+--------+
   |      1 | 32481596F | Aarón           | Rivero    | Gómez     | Desarrollo       |      120000 |   6000 |
   |      2 | Y5575632D | Adela           | Salas     | Díaz      | Sistemas         |      150000 |  21000 |
   |      3 | R6970642B | Adolfo          | Rubio     | Flores    | Recursos Humanos |      280000 |  25000 |
   |      4 | 77705545E | Adrián          | Suárez    | NULL      | Contabilidad     |      110000 |   3000 |
   |     10 | 46384486H | Diego           | Flores    | Salas     | I+D              |      375000 | 380000 |
   |     12 | 41234836R | Irene           | Salas     | Flores    | NULL             |        NULL |   NULL |
   |      9 | 56399183D | Juan            | Gómez     | López     | Sistemas         |      150000 |  21000 |
   |     13 | 82635162B | Juan Antonio    | Sáez      | Guerrero  | NULL             |        NULL |   NULL |
   |      5 | 17087203C | Marcos          | Loyola    | Méndez    | I+D              |      375000 | 380000 |
   |      6 | 38382980M | María           | Santana   | Moreno    | Desarrollo       |      120000 |   6000 |
   |     11 | 67389283A | Marta           | Herrera   | Gil       | Desarrollo       |      120000 |   6000 |
   |      8 | 71651431Z | Pepe            | Ruiz      | Santana   | Recursos Humanos |      280000 |  25000 |
   |      7 | 80576669X | Pilar           | Ruiz      | NULL      | Sistemas         |      150000 |  21000 |
   +--------+-----------+-----------------+-----------+-----------+------------------+-------------+--------+
   ```


2. ```sql
   SELECT codigo, nif, nombre, apellido1, apellido2
   FROM empleado
   WHERE codigo_departamento IS NULL;
   ```

   ```
   +--------+-----------+--------------+-----------+-----------+
   | codigo | nif       | nombre       | apellido1 | apellido2 |
   +--------+-----------+--------------+-----------+-----------+
   |     12 | 41234836R | Irene        | Salas     | Flores    |
   |     13 | 82635162B | Juan Antonio | Sáez      | Guerrero  |
   +--------+-----------+--------------+-----------+-----------+
   ```

3. ```sql
   SELECT d.codigo, d.nombre, d.presupuesto, d.gasto
   FROM departamento d
   LEFT JOIN empleado e ON d.codigo = e.codigo_departamento
   WHERE e.codigo_departamento IS NULL;
   ```

   ```
   +--------+------------+-------------+-------+
   | codigo | nombre     | presupuesto | gasto |
   +--------+------------+-------------+-------+
   |      6 | Proyectos  |           0 |     0 |
   |      7 | Publicidad |           0 |  1000 |
   +--------+------------+-------------+-------+
   ```

4. ```sql
   SELECT e.codigo AS codigo_empleado, e.nif, e.nombre AS nombre_empleado, e.apellido1, e.apellido2,
          d.codigo AS codigo_departamento, d.nombre AS nombre_departamento, d.presupuesto, d.gasto
   FROM empleado e
   LEFT JOIN departamento d ON e.codigo_departamento = d.codigo
   
   UNION
   
   SELECT NULL AS codigo_empleado, NULL AS nif, NULL AS nombre_empleado, NULL AS apellido1, NULL AS apellido2,
          d.codigo AS codigo_departamento, d.nombre AS nombre_departamento, d.presupuesto, d.gasto
   FROM departamento d
   LEFT JOIN empleado e ON e.codigo_departamento = d.codigo
   WHERE e.codigo_departamento IS NULL
   
   ORDER BY nombre_departamento;
   ```

   ```
   +-----------------+-----------+-----------------+-----------+-----------+---------------------+---------------------+-------------+--------+
   | codigo_empleado | nif       | nombre_empleado | apellido1 | apellido2 | codigo_departamento | nombre_departamento | presupuesto | gasto  |
   +-----------------+-----------+-----------------+-----------+-----------+---------------------+---------------------+-------------+--------+
   |              12 | 41234836R | Irene           | Salas     | Flores    |                NULL | NULL                |        NULL |   NULL |
   |              13 | 82635162B | Juan Antonio    | Sáez      | Guerrero  |                NULL | NULL                |        NULL |   NULL |
   |               4 | 77705545E | Adrián          | Suárez    | NULL      |                   4 | Contabilidad        |      110000 |   3000 |
   |               1 | 32481596F | Aarón           | Rivero    | Gómez     |                   1 | Desarrollo          |      120000 |   6000 |
   |               6 | 38382980M | María           | Santana   | Moreno    |                   1 | Desarrollo          |      120000 |   6000 |
   |              11 | 67389283A | Marta           | Herrera   | Gil       |                   1 | Desarrollo          |      120000 |   6000 |
   |               5 | 17087203C | Marcos          | Loyola    | Méndez    |                   5 | I+D                 |      375000 | 380000 |
   |              10 | 46384486H | Diego           | Flores    | Salas     |                   5 | I+D                 |      375000 | 380000 |
   |            NULL | NULL      | NULL            | NULL      | NULL      |                   6 | Proyectos           |           0 |      0 |
   |            NULL | NULL      | NULL            | NULL      | NULL      |                   7 | Publicidad          |           0 |   1000 |
   |               3 | R6970642B | Adolfo          | Rubio     | Flores    |                   3 | Recursos Humanos    |      280000 |  25000 |
   |               8 | 71651431Z | Pepe            | Ruiz      | Santana   |                   3 | Recursos Humanos    |      280000 |  25000 |
   |               2 | Y5575632D | Adela           | Salas     | Díaz      |                   2 | Sistemas            |      150000 |  21000 |
   |               7 | 80576669X | Pilar           | Ruiz      | NULL      |                   2 | Sistemas            |      150000 |  21000 |
   |               9 | 56399183D | Juan            | Gómez     | López     |                   2 | Sistemas            |      150000 |  21000 |
   +-----------------+-----------+-----------------+-----------+-----------+---------------------+---------------------+-------------+--------+
   ```

5. ```sql
   SELECT NULL AS codigo_empleado, NULL AS nif, NULL AS nombre_empleado, NULL AS apellido1, NULL AS apellido2,
          NULL AS codigo_departamento, NULL AS nombre_departamento, NULL AS presupuesto, NULL AS gasto
   FROM empleado
   WHERE codigo_departamento IS NULL
   
   UNION
   
   SELECT NULL AS codigo_empleado, NULL AS nif, NULL AS nombre_empleado, NULL AS apellido1, NULL AS apellido2,
          d.codigo AS codigo_departamento, d.nombre AS nombre_departamento, d.presupuesto, d.gasto
   FROM departamento d
   WHERE d.codigo NOT IN (SELECT codigo_departamento FROM empleado WHERE codigo_departamento IS NOT NULL)
   
   ORDER BY nombre_departamento;
   ```

   ```
   +-----------------+------+-----------------+-----------+-----------+---------------------+---------------------+-------------+-------+
   | codigo_empleado | nif  | nombre_empleado | apellido1 | apellido2 | codigo_departamento | nombre_departamento | presupuesto | gasto |
   +-----------------+------+-----------------+-----------+-----------+---------------------+---------------------+-------------+-------+
   | NULL            | NULL | NULL            | NULL      | NULL      |                NULL | NULL                |        NULL |  NULL |
   | NULL            | NULL | NULL            | NULL      | NULL      |                   6 | Proyectos           |           0 |     0 |
   | NULL            | NULL | NULL            | NULL      | NULL      |                   7 | Publicidad          |           0 |  1000 |
   +-----------------+------+-----------------+-----------+-----------+---------------------+---------------------+-------------+-------+
   ```

# Consultas resumen

1. ```sql
   SELECT SUM(presupuesto) AS total_presupuesto
   FROM departamento;
   ```

   ```
   +-------------------+
   | total_presupuesto |
   +-------------------+
   |           1035000 |
   +-------------------+
   ```

2. ```sql
   SELECT AVG(presupuesto) AS media_presupuesto
   FROM departamento;
   ```

   ```
   +--------------------+
   | media_presupuesto  |
   +--------------------+
   | 147857.14285714287 |
   +--------------------+
   ```

3. ```sql
   SELECT MIN(presupuesto) AS minimo_presupuesto
   FROM departamento;
   ```

   ```
   +--------------------+
   | minimo_presupuesto |
   +--------------------+
   |                  0 |
   +--------------------+
   ```

4. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento
   WHERE presupuesto = (
       SELECT MIN(presupuesto)
       FROM departamento
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | Proyectos           |           0 |
   | Publicidad          |           0 |
   +---------------------+-------------+
   ```

5. ```sql
   SELECT MAX(presupuesto) AS maximo_presupuesto
   FROM departamento;
   ```

   ```
   +--------------------+
   | maximo_presupuesto |
   +--------------------+
   |             375000 |
   +--------------------+
   ```

6. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento
   WHERE presupuesto = (
       SELECT MAX(presupuesto)
       FROM departamento
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | I+D                 |      375000 |
   +---------------------+-------------+
   ```

7. ```sql
   SELECT COUNT(codigo) AS total_empleados
   FROM empleado;
   ```

   ```
   +-----------------+
   | total_empleados |
   +-----------------+
   |              13 |
   +-----------------+
   ```

8. ```sql
   SELECT COUNT(apellido2) AS empleados_con_segundo_apellido
   FROM empleado
   WHERE apellido2 IS NOT NULL;
   ```

   ```
   +--------------------------------+
   | empleados_con_segundo_apellido |
   +--------------------------------+
   |                             11 |
   +--------------------------------+
   ```

9. ```sql
   SELECT d.nombre AS nombre_departamento, COUNT(e.codigo) AS numero_empleados
   FROM departamento d
   LEFT JOIN empleado e ON d.codigo = e.codigo_departamento
   GROUP BY d.nombre;
   ```

   ```
   +---------------------+------------------+
   | nombre_departamento | numero_empleados |
   +---------------------+------------------+
   | Desarrollo          |                3 |
   | Sistemas            |                3 |
   | Recursos Humanos    |                2 |
   | Contabilidad        |                1 |
   | I+D                 |                2 |
   | Proyectos           |                0 |
   | Publicidad          |                0 |
   +---------------------+------------------+
   ```

10. ```sql
    SELECT d.nombre AS nombre_departamento, COUNT(e.codigo) AS numero_empleados
    FROM departamento d
    LEFT JOIN empleado e ON d.codigo = e.codigo_departamento
    GROUP BY d.nombre
    HAVING COUNT(e.codigo) > 2;
    ```

    ```
    +---------------------+------------------+
    | nombre_departamento | numero_empleados |
    +---------------------+------------------+
    | Desarrollo          |                3 |
    | Sistemas            |                3 |
    +---------------------+------------------+
    ```

11. ```sql
    SELECT d.nombre AS nombre_departamento, COUNT(e.codigo) AS numero_empleados
    FROM departamento d
    LEFT JOIN empleado e ON d.codigo = e.codigo_departamento
    GROUP BY d.nombre;
    ```

    ```
    +---------------------+------------------+
    | nombre_departamento | numero_empleados |
    +---------------------+------------------+
    | Desarrollo          |                3 |
    | Sistemas            |                3 |
    | Recursos Humanos    |                2 |
    | Contabilidad        |                1 |
    | I+D                 |                2 |
    | Proyectos           |                0 |
    | Publicidad          |                0 |
    +---------------------+------------------+
    ```

12. ```sql
    SELECT d.nombre AS nombre_departamento, COUNT(e.codigo) AS numero_empleados
    FROM departamento d
    LEFT JOIN empleado e ON d.codigo = e.codigo_departamento
    WHERE d.presupuesto > 200000
    GROUP BY d.nombre;
    ```

    ```
    +---------------------+------------------+
    | nombre_departamento | numero_empleados |
    +---------------------+------------------+
    | Recursos Humanos    |                2 |
    | I+D                 |                2 |
    +---------------------+------------------+
    ```

# Subconsultas

1. ```sql
   SELECT codigo, nif, nombre, apellido1, apellido2, codigo_depart
   FROM empleado
   WHERE codigo_departamento = (
       SELECT codigo
       FROM departamento
       WHERE nombre = 'Sistemas'
   );
   ```

   ```
   +--------+-----------+--------+-----------+-----------+---------------+
   | codigo | nif       | nombre | apellido1 | apellido2 | codigo_depart |
   +--------+-----------+--------+-----------+-----------+---------------+
   |      2 | Y5575632D | Adela  | Salas     | Díaz      |             2 |
   |      7 | 80576669X | Pilar  | Ruiz      | NULL      |             2 |
   |      9 | 56399183D | Juan   | Gómez     | López     |             2 |
   +--------+-----------+--------+-----------+-----------+---------------+
   ```

2. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento
   WHERE presupuesto = (
       SELECT MAX(presupuesto)
       FROM departamento
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | I+D                 |      375000 |
   +---------------------+-------------+
   ```

3. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento
   WHERE presupuesto = (
       SELECT MIN(presupuesto)
       FROM departamento
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | Proyectos           |           0 |
   | Publicidad          |           0 |
   +---------------------+-------------+
   ```

4. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento d1
   WHERE NOT EXISTS (
       SELECT 1
       FROM departamento d2
       WHERE d2.presupuesto > d1.presupuesto
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | I+D                 |      375000 |
   +---------------------+-------------+
   ```

5. ```sql
   SELECT nombre AS nombre_departamento, presupuesto
   FROM departamento d1
   WHERE NOT EXISTS (
       SELECT 1
       FROM departamento d2
       WHERE d2.presupuesto < d1.presupuesto
   );
   ```

   ```
   +---------------------+-------------+
   | nombre_departamento | presupuesto |
   +---------------------+-------------+
   | Proyectos           |           0 |
   | Publicidad          |           0 |
   +---------------------+-------------+
   ```

6. ```sql
   SELECT nombre
   FROM departamento
   WHERE codigo = ANY (
       SELECT codigo_departamento
       FROM empleado
   );
   ```

   ```
   +------------------+
   | nombre           |
   +------------------+
   | Desarrollo       |
   | Sistemas         |
   | Recursos Humanos |
   | Contabilidad     |
   | I+D              |
   +------------------+
   ```

7. ```sql
   SELECT nombre
   FROM departamento
   WHERE codigo = ALL (
       SELECT codigo_departamento
       FROM empleado
   );
   ```

   ```
   +------------+
   | nombre     |
   +------------+
   | Proyectos  |
   | Publicidad |
   +------------+
   ```

8. ```sql
   SELECT nombre
   FROM departamento
   WHERE codigo IN (
       SELECT DISTINCT codigo_departamento
       FROM empleado
       WHERE codigo_departamento IS NOT NULL
   );
   ```

   ```
   +------------------+
   | nombre           |
   +------------------+
   | Desarrollo       |
   | Sistemas         |
   | Recursos Humanos |
   | Contabilidad     |
   | I+D              |
   +------------------+
   ```

9. ```sql
   SELECT nombre
   FROM departamento
   WHERE codigo NOT IN (
       SELECT DISTINCT codigo_departamento
       FROM empleado
       WHERE codigo_departamento IS NOT NULL
   );
   ```

   ```
   +------------+
   | nombre     |
   +------------+
   | Proyectos  |
   | Publicidad |
   +------------+
   ```

10. ```sql
    SELECT nombre
    FROM departamento d
    WHERE EXISTS (
        SELECT 1
        FROM empleado e
        WHERE e.codigo_departamento = d.codigo
    );
    ```

    ```
    +------------------+
    | nombre           |
    +------------------+
    | Desarrollo       |
    | Sistemas         |
    | Recursos Humanos |
    | Contabilidad     |
    | I+D              |
    +------------------+
    ```