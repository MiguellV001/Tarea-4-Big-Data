# Fase 2 MongoDB

## 1. Descripción del caso de uso
R//: Para este diseño se selecciona el caso de uso “Almacenamiento de datos de una red social”, ya que MongoDB es especialmente adecuado para manejar información no estructurada, altamente variable y con gran volumen, como perfiles de usuarios, publicaciones, comentarios y reacciones.
MongoDB permite escalar horizontalmente, agilizar la consulta de documentos complejos y flexibilizar la evolución del modelo de datos sin necesidad de modificar un esquema rígido.
El sistema debe permitir al administrador o usuario consultar, registrar, actualizar y eliminar productos dentro del catálogo digital.
Flujo resumido del caso de uso “colecciones país Colombia”
* El administrador ingresa al panel de gestión.
* Selecciona la opción “departamento”.
* Agrega un nuevo producto o consulta uno existente.
* El sistema almacena o actualiza la información en la base de datos MongoDB.
* Los usuarios finales pueden ver el producto desde la página de mapa en Colombia.

## 2. Diseño de la base de datos
**Coleccion:** país Colombia
Para este caso de uso se proponen las siguientes colecciones:

Explique mostrar MongoDB

*db.Estudiante.findOne();
{
  _id: ObjectId('691d03334b9e93fdec0e9794'),
  id: 1,
  nombre: 'Miguel Angel',
  sexo: 'Masculino',
  edad: 28,
  municipio: 'Funza',
  departamento: 'Cundinamarca',
  pais: 'Colombia',
  poblacion: 82000,
  'código DANE': 25286,
  'año': 2021
}*

## 3. Implementación de insertar
Implementación de usuarios

db.usuarios.insertOne ({
  id: 101,
  nombre: "Alonso",
  sexo: "M",
  edad: 46,
  municipio: "Belén de umbría",
  departamento: "Risaralda",
  pais: "Colombia",
  poblacion: 82000,
  codigo_DANE: 66088,
  anio: 2014
})
{
  acknowledged: true,
  insertedId: ObjectId('691f5b718e8a99f0c4c079d7')
}

**Implementación de Selección

db.Estudiante.find({ edad: 33})
{
  _id: ObjectId('691d160b4b9e93fdec0e9835'),
  id: 79,
  nombre: 'César',
  sexo: 'M',
  edad: 33,
  municipio: 'Ubate',
  departamento: 'Cundinamarca',
  pais: 'Colombia',
  poblacion: 82000,
  codigo_DANE: 25843,
  anio: 2025
}
{
  _id: ObjectId('691d17c14b9e93fdec0e985b'),
  id: 98,
  nombre: 'Viviana',
  sexo: 'F',
  edad: 33,
  municipio: 'Sevilla',
  departamento: 'Valle del cauca',
  pais: 'Colombia',
  poblacion: 82000,
  codigo_DANE: 76736,
  anio: 2025
}

**Implementación de Actualización

db.Estudiante.updateOne({ id: 18 }, { $set: { municipio: 'Facatativa' } });
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}

db.Estudiante.findOne({ id: 18 });
{
  _id: ObjectId('691d0e4b4b9e93fdec0e97ba'),
  id: 18,
  nombre: 'Diana',
  sexo: 'F',
  edad: 36,
  municipio: 'Facatativa',
  departamento: 'Cundinamarca',
  pais: 'Colombia',
  poblacion: 82000,
  codigo_DANE: 11001,
  anio: 2025
}

**Implementación de Eliminación de documentos

db.Estudiante.deleteOne({id: 101});
{
  acknowledged: true,
  deletedCount: 0
}

db.Estudiante.findOne({id: 101});
null
