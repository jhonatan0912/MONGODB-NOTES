- Para iniciar el servidor

```console
  $ mongod 
```

- Para conectarnos a la base de datos

```console
  $ mongosh
```
---


|MYSQL    |MONGODB    |
|---------|-----------|
|TABLAS   |COLECCIONES|
|REGISTROS|DOCUMENTOS |

___

- Comando para mostrar las base de datos
```console
  $ show dbs
```

- Comando para ver la base en la que nos encontramos
```console
  $ db
```

- Crear una base de datos
```console
  $ use <name>
```

- Insertar un dato
```js
  $ db.<name_colection>.insert({})

  Ejm:
  $ db.products.insert({"name":"laptop1"}) //insert alredy deprecated, instead use insertOne or insertMany
```

- Mostrar las colecciones que tiene la base de datos

```console
  $ show collections
```

- Eliminar la base de datos actual
```console
  $ db.dropDatabase()
```
- Crear una coleccion
```consolegit remote add origin https://github.com/jhonatan0912/MONGODB-NOTES.git
  $ db.createCollection(<name>)

  Ejm:
  $ db.createCollection("users")
```
- Eliminar una coleccion
```console
  $ db.<collection_name>.drop()

  Ejm:
  $ db.products.drop()
```
- Listar documentos de una coleccion
```console
  $ db.<collection_name>.find()
```
___
## CREATE
```console
  $ db.products.insert({"name":"laptop1"})
```
## READ
```console
  $ db.products.find() //si el documento es corto
  $ db.products.find().pretty() //si es extenso usamos pretty para verlo mejor
```
## UPDATE
```console
  $ db.products.updateOne({"price":1000},{$set:{"price":99.99}})
```
## DELETE
```console
  $ db.products.deleteOne({"price":99.99})
```
