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
## Se crea la nueva rama
```code
     git checkout -b ejercicio1-branch
Cambiado a nueva rama 'ejercicio1-branch'
```
## Creo el Ejercicio1
```java
public class Ejercicio1 {
    public static void main(String[] args) {
        System.out.println("Ejercicio 1 realizado.");
    }
}  
```
```code
git status 
En la rama ejercicio1-branch
Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        ejercicio1.java

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
     git add  Ejercicio1.java 
     git commit -m "Se incluye el Ejercicio1.java"
[ejercicio1-branch 83ea3a1] Se incluye el Ejercicio1.java
 1 file changed, 5 insertions(+)
 create mode 100644 Ejercicio1.java
```
## Subimos los nuevos cambios
```code

    git push --set-upstream origin ejercicio1-branch
Enumerando objetos: 4, listo.
Contando objetos: 100% (4/4), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 419 bytes | 419.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
remote: 
remote: Create a pull request for 'ejercicio1-branch' on GitHub by visiting:
remote:      https://github.com/alejandrosalazargonzalez/ejercicio-git-branch/pull/new/ejercicio1-branch
remote: 
To https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
 * [new branch]      ejercicio1-branch -> ejercicio1-branch
Rama 'ejercicio1-branch' configurada para hacer seguimiento a la rama remota 'ejercicio1-branch' de 'origin'.
```
## Unimos ambas ramas
```code
    git checkout main
M       README.md
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
     git merge ejercicio1-branch 
Actualizando 69d9e76..83ea3a1
Fast-forward
 Ejercicio1.java | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 Ejercicio1.java
    git push
Total 0 (delta 0), reusados 0 (delta 0), pack-reusados 0
To https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
   69d9e76..83ea3a1  main -> main
```
## Se crea la rama del ejercicio 2
```code
    git checkout -b ejercicio2-branch
Cambiado a nueva rama 'ejercicio2-branch'
```
## Se crea el ejercicio 2
```java
public class Ejercicio2 {
    public static void main(String[] args) {
        System.out.println("Ejercicio 2 realizado.");
    }
}    
```
## Hago un commit de los cambios
```code 
    git commit -m "Se incluye el Ejercicio2.java"
[ejercicio2-branch 0ad27c2] Se incluye el Ejercicio2.java
 3 files changed, 46 insertions(+), 6 deletions(-)
 create mode 100644 Ejercicio2.java
```

## Se suben los cambios al repositorio 
```code 
    git push origin ejercicio2-branch 
Enumerando objetos: 8, listo.
Contando objetos: 100% (8/8), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (5/5), listo.
Escribiendo objetos: 100% (5/5), 935 bytes | 935.00 KiB/s, listo.
Total 5 (delta 2), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ejercicio2-branch' on GitHub by visiting:
remote:      https://github.com/alejandrosalazargonzalez/ejercicio-git-branch/pull/new/ejercicio2-branch
remote: 
To https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
 * [new branch]      ejercicio2-branch -> ejercicio2-branch
```
## Fusiono la rama del ejerciocio 2 con la main
```code
    git checkout main
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
    git merge ejercicio2-branch
Actualizando 1123f03..9a56de2
Fast-forward
 Ejercicio1.java | 10 +++++-----
 Ejercicio2.java |  5 +++++
 README.md       | 60 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 3 files changed, 69 insertions(+), 6 deletions(-)
 create mode 100644 Ejercicio2.java
 ```

## Se crea la rama del ejercicio 3
```code 
    git checkout -b ejercicio3-branch
Cambiado a nueva rama 'ejercicio3-branch'
```

## Creo el ejercicio 3
```java
public class Ejercicio3 {
    public static void main(String[] args) {
        System.out.println("Ejercicio 3 realizado.");
    }
}    
```
## Commit del ejercicio 3
```code
    git commit -m "Se incluye el Ejercicio3.java"
[ejercicio3-branch c7539aa] Se incluye el Ejercicio3.java
 2 files changed, 19 insertions(+)
 create mode 100644 Ejercicio3.java
```
## Subo la rama 3 con sus cambios
```code
    git push origin ejercicio3-branch 
Enumerando objetos: 9, listo.
Contando objetos: 100% (9/9), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (7/7), listo.
Escribiendo objetos: 100% (7/7), 867 bytes | 433.00 KiB/s, listo.
Total 7 (delta 4), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote: 
remote: Create a pull request for 'ejercicio3-branch' on GitHub by visiting:
remote:      https://github.com/alejandrosalazargonzalez/ejercicio-git-branch/pull/new/ejercicio3-branch
remote: 
To https://github.com/alejandrosalazargonzalez/ejercicio-git-branch
 * [new branch]      ejercicio3-branch -> ejercicio3-branch
```

## Fusiono la rama main y la del ejercicio 3
```code
```
