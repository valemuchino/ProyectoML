# <h1 align=center> **PROYECTO MACHINE LEARNING** </h1>

>## <p>***Realizado por***: Valentino Muchino <br>
### ***Linkedin***: [https://www.linkedin.com/in/valentinomuchino/](https://www.linkedin.com/in/valentinomuchino/)<br>
### ***GitHub***: [https://github.com/valemuchino](https://github.com/valemuchino)</p>
### ***Email***: valentinogrowth@gmail.com</p>

# <h2 align=left> ***Contexto del proyecto:*** </h2>

En la sociedad actual, los precios de los inmuebles han presentado un constante cambio, por lo que quienes deseen invertir o vender una propiedad se enfrentan al fenómeno especulativo existente en la valorización de éstos. <br>

Debido al constante crecimiento de las ciudades, llega a un punto en donde no se tiene certeza de la valorización real dentro del sector en donde se desee invertir. <br>

Pese a que el precio depende, en cierta medida, de las tendencias que esté teniendo el mercado inmobiliario en un determinado tiempo, poder estimar adecuadamente el valor de una propiedad es una referencia clave para entender si es una buena oportunidad, ya sea de compra o de venta.

# <h2 align=left> ***Rol del proyecto:*** </h2>

En base a los datasets provistos, debemos proponer **2 tipos de predicciones**:

1) **Un modelo de clasificación con aprendizaje supervisado** que permita clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a su disposición.<br><br>
Para esto debe crear la columna **`category_price`**, en la cual se consideran las categorías
* **'low'**: Para precios entre 0 y 999 dólares.
* **'medium'**: Para precios entre 1000 y 1999 dólares.
* **'high'**: Para precios desde 2000 dólares en adelante.<br><br>
​Considerando esta categorización, el **objetivo es predecir si una propiedad pertenece a la categoría de precios bajos (low).**

2) Implementar **un modelo de clasificación con aprendizaje no supervisado**, utilizando clustering que agrupe los inmuebles según las **3 categorias** a las que pueden pertenecer. Para ello, solo usaran el dataset de test provisto, eliminando previamente las caracteristicas que presenten nulos.

# <h2 align=left> ***Archivos provistos:*** </h2>

Se proveen los siguientes archivos en formato parquet:
 - **'train.parquet'**: Contiene 346479 registros y 22 dimensiones, el cual incluye la información **numérica** del precio en la columna `price`.
 - **'test.parquet'**: Contiene 38498 registros y 21 dimensiones, el cual no incluye la información del precio.

# <h2 align=left> ***Descripción de los features:*** </h2>

- **`id`**: Identificador del anuncio. 
- **`url`**: Link web del anuncio.
- **`region`**: Región de Estados Unidos en donde se encuentra la propiedad.
- **`region_url`**: Link web de los anuncios pertenecientes a la región. 
- **`price`**: Precio de la propiedad en dólares.
- **`type`**: Tipo de propiedad.
- **`sqfeet`**: Pies cuadrados de la propiedad.
- **`beds`**: Cantidad de dormitorios.
- **`baths`**: Cantidad de baños.
- **`cats_allowed`**: Si se permiten gatos en la propiedad toma el valor 1, 0 para caso contrario.
- **`dogs_allowed`**: Si se permiten perros en la propiedad toma el valor 1, 0 para caso contrario.
- **`smoking_allowed`**: Si se permite fumar en la propiedad toma el valor 1, 0 para caso contrario.
- **`wheelchair_access`**: Si la propiedad posee acceso para sillas de ruedas toma el valor 1, 0 para caso contrario.
- **`electric_vehicle_charge`**: Si la propiedad posee cargador para vehículos eléctricos toma el valor 1, 0 para caso contrario.
- **`comes_furnished`**: Si la propiedad viene amueblada toma el valor 1, 0 para caso contrario.
- **`laundry_options`**: Opciones de lavandería (w/d in unit: Lavadora/secadora en la propiedad, w/d hookups: conexión para lavadora/secadora, laundry on site: servicio de lavandería en el lugar, laundry in bldg: servicio de lavandería en el edificio, no laundry on sit: sin servicio de lavandería).
- **`parking_options`**: Opciones de estacionamiento (off-street parking: zona de estacionamiento, attached garage: garaje incluido, carport: cochera/garaje abierto, detached garage: garaje separado, street parking: estacionamiento delimitado en la calle, no parking: sin estacionamiento, valet parking: estacionamiento con servicio valet).
- **`image_url`**: Link web de la imagen de la propiedad en el anuncio. 
- **`description`**: Descripción de la propiedad puesta en el anuncio. 
- **`lat`**: Latitud.
- **`long`**: Longitud.
- **`state`**: Código del estado al que pertenece la propiedad.