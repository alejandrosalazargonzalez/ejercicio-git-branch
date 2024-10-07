# Entornos de Desarrollo: Comenzando con Git "Trabajando con Branchs"

## Clonación del repositorio

```code
 git clone https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
Clonando en 'ejercicio-git-branch'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Recibiendo objetos: 100% (3/3), listo.
```
## Se incluye el commit
```code
 git commit -m "se incluye la descripción inicial de la tarea"
[main f54a47d] se incluye la descripción inicial de la tarea
 1 file changed, 13 insertions(+), 1 deletion(-)
 rewrite README.md (100%)
```
## Se suben los cambios
```code
 git push
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 531 bytes | 531.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
To https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
   c362c87..f54a47d  main -> main
```