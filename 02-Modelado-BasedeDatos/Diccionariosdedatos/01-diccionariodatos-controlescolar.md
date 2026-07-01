# Diccionario de Datos de la Base de Datos Control Escolar

1. Información General 

| Elemento | Valor |
| :--- | :--- |
| Proyecto | Control Escolar |
| Versión | 1.0 |
| Fecha | Junio 2026 |
| Elaboró | Alondra Denisse Gaytan Gonzalez | 
| SGBD | SQLSERVER |

2. Descripción de la Base de Datos

La Base De Datos Administra:

- Carrera
- Alumno
- Profesor
- Materia
- Grupo
- Inscripción

Permite controlar la oferta académica y la inscripción de estudiantes

3. Catálogo de Restricciones Utilizadas

| Catalogo | Significado |
| :--- | :--- |
| PK | Primary Key |
| FK | Foreign Key |
| NN | Not Null |
| UQ |  Unique |
| AI | Autoincrement o Identity |
| CK | Check |
| DF | Default |

4. Diccionario de Datos

**Tabla:** _Carrera_

**Descripción**

Almacena las carreras ofertadas por la Universidad

| Campo | Tipo | Longitud | Restricciones  | Descripcion |
| :--- | :--- | :--- | :--- | :--- |
| id_carrera | INT | - | PK, AI, NN | Identificador unico de la carrera|
| nombre | VARCHAR | 100 | UQ, NN | Nombre de la carrera |
| duracion_cuatrimestre | INT | - | NN, CK (>0) | Duracion en cuatrimestre |

--- 

**Tabla:** _Alumno_

**Descripción**

Almacena la información de los estudiantes

| Campo | Tipo | Longitud | Restricciones  | Descripcion |
| :--- | :--- | :--- | :--- | :--- |
| id_alumno | INT | - | PK, AI, NN | Identificador del alumno|
| matricula | VARCHAR | 10 | UQ, NN | Matricula institucional |
| nombre | VARCHAR | 50 | NN | Nombre del alumno |
| apellido_paterno | VARCHAR | 50 | NN | Apellido Paterno  |
| apellido_materno | VARCHAR | 50 | Null | Apellido Materno  |
| correo | VARCHAR | 100 | UQ, NN | Correo Institucional |
| fecha_nacimiento | Date | - | NN | Fecha Nacimiento |
| id_carrera | INT | - | FK, NN | Carrera a la que pertenece |


--- 

TODO: Documentar las siguientes tablas

5. Relaciones en la Base de Datos

| Relación  | Cardinalidad  | Descripción  |
| :--- | :--- | :--- |
| Carrera -> Alumno  | 1:N  | Una materia tiene muchos alumnos |
| Carrera -> Materia  | 1:N  | Una carrera tiene muchas materias |
| Profesor -> Grupo  | 1:N  | Un profesor puede impartir en varios grupos |
| Materia -> Grupo  | 1:N  | Una materia puede abrirse en varios grupos |
| Alumno -> Inscripcion  | 1:N  | Un alumno puede tener varias inscripciones |
| Grupo -> Inscripcion  | 1:N  | Un grupo puede tener muchos alumnos |

---

6. Matriz de Claves Foraneas

| Tabla  | Campo FK  | Referencia  |
| :--- | :--- | :--- |
| Alumno  | id_carrera  | Carrera(id_carrera) |
| Materia  | id_carrera  | Carrera(id_carrera) |
| Grupo  | id_profesor  | Profesor(id_profesor) |
| Grupo  | id_materia  | Materia(id_materia) |
| Inscripcion  | id_alumno  | Alumno(id_alumno) |
| Inscripcion  | id_grupo  | Grupo(id_grupo) |


7. Integridad referencial

| Clave  | Regla  |
| :--- | :--- |
| IR-01  | No se puede registrar un alumno con una carrera inexistente  |
| IR-02  | No se puede crear un grupo para una materia inexistente  |
| IR-03  | No se puede crear un grupo para un profesor inexistente  |

---

8. Reglas del Negocio

| Clave  | Regla  |
| :--- | :--- |
| RN-01  | Un alumno pertenece a una sola carrera  |
| RN-02  | Una carrera puede tener muchos alumnos  |
| RN-03  | Una carrera puede tener muchas materias |
| RN-04  | Un profesor puede impartir varios grupos   |

---

9. Diagrama Relacional

![EjercicioRelacional](../../img/)