# proyectoManejoGit
Proyecto del modulo de Desarrollo de Software del Diplomado Linux Embebido 3era. Gen.

En archivo gitlog.txt se verá un gráfico obtenido con la salida del comando
$git log --pretty=oneline --graph

Aquí explicaremos donde se encuentran las 3 principales uniones que git ofrece:
Merge, rebase y cherrypick.

-Rebase: En el commit c7fa49b (abrv. del chechsum del mismo), fue donde hicimos nuestro primer rebase.
  La rama donde proviene este commit, que agrega el nombre de Marco a Integrantes.txt, parte del segundo
  commit del arbol. Nos podemos dar cuenta porque el commit 692b500 describe la misma acción, pero con la 
  difencia que su checksum es diferente. ¿Cómo es posible? El commit del rebase se origino cuando git recibio 
  el comando $git rebase, y lo que git hizo fue reorganizar el git log de tal manera que su arbol se viera como
  una sola rama (esta es la función del git rebase). Para hacer notar esto, se hizo un merge (f7836cb) donde 
  se unió el commit con el checksum original (692b500) y se concluye que la rama principal es producto de un
  $git rebase marco (hecho en la rama master) hasta el commit c7fa49b.

-Merge: La unión de la rama de Felix se unió con $git merge, como se ve en el commit ()

-Cherry-pick: El primer commit que se eligió provenía de la rama de Samuel tenía el checksum cea90b8 y cuando 
se unio a la rama master tenía el checksum d1fcf41. Tambíén se hizó otro cherrypick con commit 28ed8e2 proveniente
de la rama de Samuel. El cherry-pick se ejecutó con $git cherry-pick <hash-commit> desde la rama master.

**Resumen:
  - El rebase se obtuvo a partir de la rama de Marco. commit(c7fa49b)
  - La rama de Felix se unió con un merge. commit()
  - El cherry-pick se obtuvo de un commit de la rama de Samuel. commit (1fcf41)
