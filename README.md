# Actividad práctica: Presentaciones vía Pull Request

## Objetivo
Aprender a trabajar con Git y GitHub siguiendo un flujo completo de trabajo.

---

## Instrucciones paso a paso

1. **Clona el repositorio y revisa la configuración del remoto**
   ```bash
   git clone git@github.com:campus-CodeArts/Actividad-Pr-ctica-Github.git
   cd Actividad-Pr-ctica-Github
   git remote -v        # verifica la URL del repositorio
   git branch           # muestra las ramas locales
   ```

2. **Crea tu rama personal**
   ```bash
   git checkout -b rama/nombredelalumno
   git status           # comprueba el estado del repositorio
   ```

3. **Edita `plantilla.md` para añadir tu nombre en tu grupo**
   - Si estás en DAW y perteneces al grupo Koala, añade `Nombre Apellido (Koala)` debajo del encabezado de DAW.
   - No borres a tus compañeros.

4. **Revisa los cambios antes de confirmarlos**
   ```bash
   git diff plantilla.md
   ```

5. **Registra el cambio en el repositorio**
   ```bash
   git add plantilla.md
   git commit -m "Añadida presentación de Nombre Apellido (DAW)"
   git log --oneline -1  # muestra el último commit
   ```

6. **Envía tu rama al repositorio remoto**
   ```bash
   git push origin rama/nombredelalumno
   git branch -a        # verifica que tu rama remota esté disponible
   ```

7. **Abre un Pull Request en GitHub**
   1. Ve al repositorio en GitHub.
   2. Haz clic en `Compare & pull request`.
   3. Revisa que la base sea `main` y la comparación sea tu rama.
   4. Escribe un título descriptivo y crea el pull request.

8. **Fusiona tu Pull Request**
   1. Una vez aprobado, utiliza `Merge pull request` y confirma.

9. **Actualiza tu rama `main` local**
   ```bash
   git checkout main
   # si estabas trabajando en otra rama y tienes cambios sin confirmar
   git stash push -m "trabajo en progreso"
   git pull origin main
   git checkout rama/nombredelalumno
   git stash pop
   ```

10. **Limpia ramas locales que ya no uses**
    ```bash
    git branch -d rama/nombredelalumno
    ```

11. **Ejercicios adicionales en equipo**
    1. Trabaja en parejas y crea una rama colaborativa.
    2. Realiza cambios independientes y usa `git pull --rebase` para integrarlos.
    3. Si surge un conflicto, resuélvelo y registra el merge con un commit.
    4. Practica `git stash` para guardar cambios temporales mientras revisas otra rama.
    5. Una vez fusionada la rama, revisa el historial con `git log --graph`.

---

## Notas importantes

- No modifiques otras partes del archivo.
- Mantén el orden alfabético por grupo.
- Espera a que el profesor revise y apruebe tu PR.

---

Buena suerte
