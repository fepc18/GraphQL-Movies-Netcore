# gql-movies

Tipos
Los tipos requieren un poco de repetitivo. Primero debe crear una clase básica para encapsular los datos que describen su objeto, luego usar esto para extender ObjectGraphTypey describir los campos que desea publicar.

El ObjectGraphTypeacepta un tipo de objeto por debajo de ella. Esto escribe el parámetro en la función de devolución de llamada de Field. Utiliza esto para describir el objeto GraphQL que se puede consultar. Deriva el tipo de campo del tipo de propiedad que devuelve.
También puede hacer cosas más complejas para escribir propiedades explícitamente y agregar miembros que no existen en el objeto subyacente.
Por ResultsTypeejemplo, define un campo para la resultsmatriz. Esto es para que pueda anidar tipos y tener una clase Result con List<Movie>y devolver a ListGraphType<MovieType>desde la consulta GraphQL.
  
Consultas
Las consultas se definen de la misma manera que los campos. Solo puede haber un objeto de consulta, pero esto no significa que no pueda dividir ese objeto de consulta.
