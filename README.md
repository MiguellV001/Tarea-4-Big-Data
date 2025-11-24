# Fase 2 MongoDB

## 1. Descripción del caso de uso
R//: Para este diseño se selecciona el caso de uso “Almacenamiento de datos de una red social”, ya que MongoDB es especialmente adecuado para manejar información no estructurada, altamente variable y con gran volumen, como perfiles de usuarios, publicaciones, comentarios y reacciones.
MongoDB permite escalar horizontalmente, agilizar la consulta de documentos complejos y flexibilizar la evolución del modelo de datos sin necesidad de modificar un esquema rígido.
El sistema debe permitir al administrador o usuario consultar, registrar, actualizar y eliminar productos dentro del catálogo digital.
Flujo resumido del caso de uso “colecciones país Colombia”
* •	El administrador ingresa al panel de gestión.
* •	Selecciona la opción “departamento”.
* •	Agrega un nuevo producto o consulta uno existente.
* •	El sistema almacena o actualiza la información en la base de datos MongoDB.
* •	Los usuarios finales pueden ver el producto desde la página de mapa en Colombia.

## 2. Diseño de la base de datos
**Coleccion:** país Colombia
Para este caso de uso se proponen las siguientes colecciones:
