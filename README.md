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

