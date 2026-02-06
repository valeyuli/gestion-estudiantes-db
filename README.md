Integrantes:
Galarza Yuliana,
Aguiar Adnery,
Espinoza Parrales,
Mateo Chelsea

---

## 1. Contexto del Problema 
**Descripción del problema:** Actualmente, el registro de información académica en muchas instituciones se realiza de forma manual mediante cuadernos o archivos físicos. Esto genera una alta vulnerabilidad a la pérdida de datos, duplicidad de registros y una ineficiencia crítica al momento de buscar o actualizar información de un estudiante específico.

**Importancia:** La digitalización de estos procesos es vital para garantizar la integridad de la información y reducir los tiempos de respuesta administrativa.

**Contexto de uso:** La aplicación está diseñada para ser utilizada por personal administrativo o docentes en un entorno escolar, proporcionando una interfaz gráfica (GUI) intuitiva que no requiere conocimientos técnicos avanzados para su operación.

---

## 2. Análisis de Requerimientos 
El sistema implementa las siguientes funcionalidades principales, alineadas a las necesidades del usuario:

* **Registro Automatizado:** Captura de datos esenciales (Nombre, ID, Edad, Curso) a través de un formulario gráfico.
* **Validación de Datos en Tiempo Real:** Implementación de manejo de excepciones (`try-catch`) para asegurar que campos como la 'Edad' solo acepten valores numéricos, evitando errores de ejecución.
* **Almacenamiento Dinámico:** Uso de la estructura de datos `ArrayList` para gestionar objetos de la clase `Estudiante` de forma eficiente en la memoria volátil.
* **Visualización Estructurada:** Presentación inmediata de los datos registrados en un componente `JTable`, permitiendo una auditoría visual rápida de los registros.

---

## 3. Diagrama de Flujo de la Aplicación 
El flujo del sistema garantiza que no existan procesos huérfanos y que el usuario siempre tenga el control:

1.  **Inicio:** Ejecución de la clase `FrmPrincipal`.
2.  **Ingreso de Datos:** El usuario completa los campos del formulario.
3.  **Validación:** El sistema verifica si los datos son correctos (ej. Edad es número).
    * *Si es incorrecto:* Muestra un mensaje de error y retorna al formulario.
    * *Si es correcto:* Crea el objeto `Estudiante`, lo añade al `ArrayList` y actualiza la tabla.
4.  **Fin/Ciclo:** El usuario puede realizar un nuevo registro o cerrar la aplicación.



---

## 4. Diseño de Interfaz y Validaciones 
La interfaz se desarrolló utilizando **Java Swing**, cumpliendo con los estándares de diseño adecuado:
* **Componentes:** Uso de `JLabel`, `JTextField`, `JButton` y `JScrollPane` con coordenadas precisas para una visualización limpia.
* **Validaciones:** El sistema incluye diálogos de alerta (`JOptionPane`) para informar al usuario sobre el éxito del registro o errores de entrada de datos.

---

## 5. Acceso a Datos y Funcionalidades Clave 
El proyecto cumple con el uso correcto de estructuras de datos orientadas a objetos:
* **Clase Estudiante:** Define el modelo de datos con encapsulamiento.
* **Colecciones:** El uso de `ArrayList<Estudiante>` permite un manejo de datos alineado totalmente con la propuesta y el diagrama de flujo presentado.
