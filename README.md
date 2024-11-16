Santiago Anaya Adan Ismael 

**1.- Explicación de Creación de Aplicación**

La presente práctica consiste en la creación de un proyecto en Angular V18, el desarrollo de esta actividad consistirá en consumir una API de usuarios, mostrandola en la ejecución, los pasos desarrollados para la creación del proyecto son:

1.1.- Creación del proyecto

![image](https://github.com/user-attachments/assets/967a21e0-a364-4c9e-a24e-bd74a805d5f8)
Este cuenta con la instrucción
ng new consumo-api-AISA --no-standalone (La parte --no-standalone) se especifica para la 
creación de un proyecto sin la característica standalone que implementa una nueva manera de creación de proyecto sin el archivo module.ts, pero para este proyecto si será necesario este archivo

Ingreso dentro de la carpeta del proyecto:

![image](https://github.com/user-attachments/assets/cdc93e2e-787d-41e0-ade5-2f3a1c4d8fc1)

1.2.- Creación del servicio user.service
Mediante el uso del comando: ng generate service services/user, se crea la carpeta "services" con los archivos necesarios para la creación del servicio de consulta de API

![image](https://github.com/user-attachments/assets/51c8c7d5-4052-44e8-b756-7f2202fcf239)

1.3.- Configuración del archivo "user.service.ts"
Este archivo se encarga de la gestión de la comunicación con la API extena, que se especifica dentro de la veriable privada "apuUrl", siendo esta: 'https://api.escuelajs.co/api/v1/users'

![image](https://github.com/user-attachments/assets/e8457ae6-a30e-4be7-99ac-df5f7c2d8a82)

1.4.- Configuración del archivo "app.module.ts"
Este archivo se encarga de la configuración y definición de los componentes, servicios y modulos que se utilizan en la aplicación, haciendo la importaión del servicio "HttpClientModule" para la creación de solicitudes HTTP dentro del programa

![image](https://github.com/user-attachments/assets/d1e3350c-175a-4fc9-bc23-ca57e353c76b)

1.5.- Creación del componente "User-List"
Mediante el uso del comando "ng generate component components/user-list" se hará la creación del componente necesario para mostrar la lista de usuarios desde el servicio anteriormente creado.

![image](https://github.com/user-attachments/assets/89982563-7bd5-4b89-8642-5c6559019668)

1.6.- Configuración del archivo "user-list.component.html" este se encargará de mostrar la tabla de elementos obtenidos de la API

![image](https://github.com/user-attachments/assets/79203eec-a723-4471-9d73-6e5aab512578)

1.7.- Ejecución
Agregando al archivo "app.compoent.html" la ruta del componente creado <app-user-list></app-user-list> y haciendo uso de la instrucción "ng serve" para correr el programa se puede visualizar la tabla de elementos botenidos de la API

![image](https://github.com/user-attachments/assets/6d806c51-4274-4b26-91e6-677a52f3b7a7)

**2.- Integración de paginación**
La integración de paginación dentro del proyecto es importante debido a que permite tener una mejor presentación de la información cuando esta es muy grande, esta es implementada mediante el uso de "MatPaginator", implementación de material design, que permite la paginación de elementos de forma sencilla 
component.ts:

![image](https://github.com/user-attachments/assets/c3ec9792-a15c-4a23-8ce7-c8432cb06fb0)
component.html:

![image](https://github.com/user-attachments/assets/3ffc343d-d086-4729-a2b5-abd682c7b193)
Implementación de cantidad de elementos de paginación

![image](https://github.com/user-attachments/assets/05089a34-d9ff-4991-a56a-5cdde6b5ad3c)

**3.- Pruebas realizadas**
![image](https://github.com/user-attachments/assets/c5045b72-f493-4f8c-a17f-ec6901d0deb3)

![image](https://github.com/user-attachments/assets/70610689-941b-4054-9064-ccc7b77d4399)

**Preguntas propuestas**
•	¿Qué hace el método getUsers en este servicio?
El método se encarga de realizar una petición para obtener el arreglo de información desde la API que se ingresó.

•	¿Por qué es necesario importar HttpClientModule?
Es necesario importar el modulo debido a que proporciona funcionalidades para que Angular pueda realizar peticiones HTTP. Sin este módulo no se podría consumir la API y no funcionaria 

•	¿Qué función cumple el método ngOnInit en el componente UserListComponent?
El método cumple con el propósito de obtener los datos de los usuarios y asignarlos a la variable llamada users inicializada anteriormente para poder mostrarlos en la vista.

•	¿Para qué sirve el bucle *ngFor en Angular?
Permite iterar sobre el arreglo, recorriendo el arreglo de usuarios generando los datos sobre las columnas Id, Name, Email, Role, mostrando todos los datos obtenidos de cada usuario en la Api.

•	¿Qué ventajas tiene el uso de servicios en Angular para el consumo de APIs?
Angular proporciona una forma organizada de manejar el consumo de APIS´S, permite separa la obtención y manipulación de la información de los componentes, facilitando el mantenimiento de código, además de que los servicios pueden ser utilizadas en diferentes componentes, ayudando a la reutilización de código y componentes.

•	¿Por qué es importante separar la lógica de negocio de la lógica de presentación?
Mejora el modularidad y la claridad del código, permitiendo especializar los componentes en una única función, separando los componentes y servicios, siendo los primeros los que se encargan en presentar los datos y los segundos encargados de obtener y manipular la información obtenida

•	¿Qué otros tipos de datos o APIs podrías integrar en un proyecto como este?
Como fue mencionado en clase se pueden incluir Apis que proporcionen información de productos, información del tiempo, estadísticas de diferentes tipos, datos sobre estados o información geográfica, etc. Son un gran campo el que puede integrar una API


