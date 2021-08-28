![Banner](./imagenes/banner.png)

# PROYECTO 3: Tablero de Datos ("Dashboard")

## **ÍNDICE**

* [1. Intro](#1-intro)
* [2. Back End](#2-Back)
* [3. Front End](#3-Front)
* [4. Operation](#4-Operation)
* [5. Demo Screenshot](#5-Demo)
* [6. Parnerts](#6-Partners)


## 1. Intro

Desarrollar una aplicación realizando una conexión a un API (financiera, educativa, social) y presentar datos en una interfaz.

Para este proyecto se utiliza la API de COVID-19, Aquí puede ver la descripción de la misma:
"https://github.com/M-Media-Group/Covid-19-API"


## 2. Back End

1. Crear carpeta back
2. Iniciar proyecto
   npm init -y
3. Crear archivo con el nombre "getDataCovid.js"
4. Configurar package.json
    - [] Agregar línea: "type": "module"
    - [] Agregar llamado del script en sección scripts: "server": "node ./back/getDataCovid.js"
    - [] Agregar dependencias:
        - [] express : npm i express
        - [] dotenv : nmp i dotenv
        - [] axios : npm i axios
        - [] cors : npm i cors
5. Configurar .env
    - [] Agregar puerto : PORT=3000
    - [] Agregar baseUrl: API_BASE_URL="https://covid-api.mmediagroup.fr"
    - [] Agregar url: API_URL="/v1/%value%?"
6. Generar listener para:
    - [] /stats : Responde a información general de un país acerca de status confirmed, deaths and recovered
                  El status recovered ya no esta siendo actualizado
    - [] /hist : Responde a información de un pais por status e histórico de fechas
    - [] /vac : Responde a información sobre la población inoculada de un país en especifíco
7. Ejecutar Server
    - [] Dentro de la carpeta back ejecutar el siguiente comando: npm run server

8. Después de descargar los archivos se debe considerar lo siguiente:
    - [] Ejecutar el comando: npm i o npm install
    - [] Agregar el archivo .env para que la configuración pueda ser parseada y leída

    
## 3. Front End

1. Generar carpeta front
2. Crear archivo app.js
3. Crear archivo index.html
4. Crear archivo styles.css
5. Archivo app.js
    - [] Función initCharts
        - [] Permite obtener datos para generar listas que alimentaran los dropdowns de Country & Status 
    - [] Función getData
        - [] Realiza los llamados a /stats, /hist & /vac
6. Archivo index.html
    - [] Agregar CDN de boostrap: https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css
    - [] Agregar script de axios: https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js
    - [] Agregar script de Chart.js: https://cdn.jsdelivr.net/npm/chart.js@3.5.1/dist/chart.min.js
    - [] Agregar script app.js: '<script type="text/javascript" src="app.js"></script>'
7. Archivo styles.css
    - [] Agregar estilos para la forma y spinner


## 4. Operation

1. Por default se mostrarán los datos de México
    - [] Datos generales del país
    - [] Datos de las personas inoculadas
    - [] Datos historicos de los últimos 15 días, solo se muestran los status confirmed & deaths
         El status recovered ya no se debe mostrar debido a que ya no esta actualizado.
2. Debe poner al menos los datos de País y Status para poder realizar una búsqueda
3. En caso de no llenar los campos de Fecha Inicial y Fecha Final entonces se toman los últimos quince días,
   Es decir se toma como Fecha Final el día actual y como Fecha Inicial el día actual menos 15 días.

## 5. Demo-Screenshot

Muestra del resultado de la consulta a través del API COVID-19
![imagen](./imagenes/imageDemo.png)

## 6. Partners

- [] Team 2
    - [] Carolina Pérez
    - [] Itzel Angélica Ibañez Miranda
    - [] Alan José Abarca Velázquez
    - [] Alberto Miranda Pacheco
    - [] Gerardo Paxtian Torres
    - [] Jorge Angel Novoa
    - [] Martín Barrera
    - [] Omar Rodrigo Orozco Camarena
    - [] Raúl Eduardo Trejo Suárez
    - [] José Antonio Salinas Ochoa