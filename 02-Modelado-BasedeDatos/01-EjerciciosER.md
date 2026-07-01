# Ejercicios del Modelo E-R

## Ejercicio 1.

Un hospital registra información de sus pacientes:
> De cada **paciente** se almacena:
- Número de paciente que lo identifica
- Nombre
- Fecha de Nacimiento

> De cada **expediente médico** se almacena:
- Número de expediente
- Fecha de apertura
- Tipo de sangre

> Reglas del negocio:
1. Cada paciente debe tener exactamente un expediente médico
2. Cada expediente médico pertenece a un único paciente
3. No puede existir un expediente sin un paciente
4. No pueder existir un paciente sin expediente

> Que se debe realizar:
- Identificar las entidades
- Identificar los atributos
- Dibujar las relaciones
- Determinar la cardinalidad
- Determinar la participación de cada entidad

![Ejercicio1](../img/ER/EjerER1.png)

## Ejercicio 2.

Una Universidad administra profesores y cursos

> De cada **profesor** se almacena:
- Número de profesor
- Nombre
- Especialidad

> De cada **curso** se almacena:
- Número de curso
- Nombre del curso
- Créditos

> Reglas del negocio
1. Un profesor puede impartir varios cursos
2. Un curso solamente puede ser impartido por un profesor
3. Puede existir un profesor que actualmente no imparta cursos
4. Todo curso debe estar asignado a un profesor

![Ejercicio2](../img/ER/EjerER2.png)

## Ejercicio 3.

Una escuela administra alumnos y materias

> De cada **alumno** se almacena:
- Matricula
- Nombre
- Semestre

> De cada **materia** se almacena:
- Clave de la materia
- Nombre de la materia
- Créditos

> Reglas del negocio
1. Un alumno puede inscribirse en varias materias
2. Una materia puede tener muchos alumnos inscritos
3. Puede existir una materia sin alumnos inscritos
4. Todo alumno debe estar inscrito en al menos una materia
5. De cada inscripción se desea almacenar:
    - Fecha de inscripción 
    - Calificación final

Nota: A la relación nombrarla **INSCRIBE**

![Ejercicio3](../img/ER/EjerER3.png)

## Ejercicio 4.

Una empresa dedicada a las ventas al por mayor necesita registrar lo siguiente:

> Para los clientes:
- Número de cliente
- Nombre (El cual es una persona moral)

>Pedidos:
- Número de pedido
- Fecha de pedido

>Productos:
- Número de producto
- Nombre
- Precio

> Reglas del negocio:
1. Un cliente puede realizar muchos pedidos
2. Cada pedido pertenece a un solo cliente
3. Un pedido contiene varios productos
4. Un producto puede aparecer en muchos pedidos
5. Un pedido debe contener al menos un producto
6. Un producto puede no haber sido vendido
7. El detalle del pedido no existe sin pedido
8. El detalle del pedido non existe sin producto
9. El detalle almacena la cantidad vendida y el precio de venta

![Ejercicio4](../img/ER/EjerER4.png)

## Ejercicio 5
> The company...
1. The company is organized into departments. Each department has a unique name, a 
unique number, and a particular employee who manages the department.We keep track 
of the start date when that employee began managing the department. A department 
may have several locations. 

> A department...
2. A department controls a number of projects, each of which has a unique name, a unique 
number, and a single location. 

> Employee´s
3. We store each employee's name, Social Security number, address, salary, sex (gender), 
and birth date. An employee is assigned to one department, but may work on several 
projects, which are not necessarily controlled by the same department. We keep track of 
the current number of hours per week that an employee works on each project. We also 
keep track of the direct supervisor of each employee (who is another employee). 

> Dependents
4. We want to keep track of the dependents of each employee for insurance purposes.We 
keep each dependent's first name, sex, birth date, and relationship to the employee. 

![Ejercicio5](../img/ER/EjerciER5.png)

## Ejercicio 6

![Ejercicio6](../img/ER/EjerER6.jpeg)