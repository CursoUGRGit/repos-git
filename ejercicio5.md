## Subversion y GIT

Cuando se habla de control de versiones, hay dos grandes formas de encarar el tema: **centralizado o distribuido.**

Lo primero que hay que aclarar es que ni Git es del todo "distribuido" (ya que se suele mantener un repositorio centralizado), ni Subversion es totalmente centralizado (porque se trabaja sobre una copia local). La diferencia en realidad es donde ocurren las operaciones (branch, commit, etc.). En el caso de Git (y los demás que son distribuidos como Mercurial), las operaciones son locales, mientras que en Subversion ocurren en el servidor.

Esto quiere decir que en Git puedo hacer N commits antes de mandar los cambios al servidor, mientras que en Subversion cada commit se hace en el servidor.

Algunas consecuencias de esto son que:

1. En Subversion los números de cada revisión son consecutivos, mientras que en Git cada commit se identifica con un UUID
2. En Git puedo hacer commits intermedios, sin necesidad de tener una versión "estable", porque puedo hacer el push al final. En Subversion, cuando hago un commit tengo que tener una versión consistente antes de hacer el commit para no romper nada que pueda necesitar alguien más. Ese commit puede ser eventualmente bastante grande.

Otra diferencia es que en el caso de Git, no es posible hacer un "checkout" parcial, lo que es bastante natural en Subversion. Por lo tanto, si el repositorio es grande, obtener la versión inicial puede ser bastante más costoso con Git.

Una de las cosas que no me convencen del todo de Subversion, es que no puedo dejar un cambio por la mitad, para hacer por ejemplo un arreglo en la última versión estable. En Git, aunque tenga cambios pendientes, puedo moverlos a un nuevo branch, arreglar lo que sea que estuviera roto, y volver a poner arriba de eso los cambios que moví temporalmente. En Subversion, la mejor alternativa que encontré a esto, sería hacer un checkout en otro directorio para hacer el arreglo ahí.

Eso nos lleva a otra diferencia: en Git hacer un branch es totalmente natural. De hecho, cada copia local puede verse como un branch. Llevado al extremo, hay quienes hacen un branch para cada nueva feature que van a estar trabajando. En Subversion, un branch se usa solamente para congelar una versión, y no es posible hacerlo de forma local.

Artículo sacado de: [http://blog.marcoscrispino.com/2011/06/subversion-vs-git.html](http://blog.marcoscrispino.com/2011/06/subversion-vs-git.html "http://blog.marcoscrispino.com/2011/06/subversion-vs-git.html")