# ProjectGIT

## 📘 Introducción al Curso Git y GitHub

Bienvenido a tu resumen personal de **Git** y **GitHub**. Aquí encontrarás los conceptos clave, comandos esenciales y buenas prácticas para dominar el control de versiones y la colaboración.

---

## 📂 Control de Versiones

**¿Qué es?**

El control de versiones registra el historial de cambios de los archivos de un proyecto, indicando qué se modificó, quién lo hizo y cuándo.

**Beneficios:**

* 💾 **Historial completo:** Recupera versiones anteriores.
* 🔒 **Seguridad:** Cada cambio queda registrado.
* ⚡ **Eficiencia:** Solo almacena diferencias.

---

## 🕰 Historia de Git y GitHub

| Año   | Evento                                         |
| ----- | ---------------------------------------------- |
| 1990s | Primeros sistemas de versiones                 |
| 2005  | Linus Torvalds crea **Git**                    |
| 2008  | Nace **GitHub**                                |
| 2018  | Microsoft adquiere GitHub                      |
| 2024  | Git y GitHub dominan la industria del software |

---

## 🔧 Git vs GitHub

| Concepto | Git                                         | GitHub                                      |
| -------- | ------------------------------------------- | ------------------------------------------- |
| Tipo     | Sistema de control de versiones distribuido | Plataforma web para alojar repositorios Git |
| Uso      | Gestión de cambios en local                 | Colaboración remota, pull requests e issues |
| Ejemplo  | `git commit -m "Mensaje"`                   | `git push origin main`                      |

---

## 🚀 Primer Proyecto Git

1. **Crear carpeta y entrar**

   ```bash
   mkdir miproyecto && cd miproyecto
   ```
2. **Inicializar repositorio**

   ```bash
   git init
   ```
3. **Crear README y agregar**

   ```bash
   echo "# Mi Proyecto" > README.md
   git add README.md
   ```
4. **Primer commit**

   ```bash
   git commit -m "Primer commit"
   ```
5. **Conectar con GitHub** (opcional)

   ```bash
   git remote add origin <URL>
   git push -u origin main
   ```

> **Verificar commits:**
>
> ```bash
> git log --oneline
> ```

---

## 💻 Instalación de Git en Windows

1. Descarga el instalador en [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Ejecuta el `.exe` y acepta las opciones predeterminadas.
3. Selecciona **Use Git from the Windows Command Prompt**.
4. (Opcional) Configura tus datos:

   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tuemail@example.com"
   ```
5. Verifica la versión:

   ```bash
   git --version
   ```

---

## 🔄 Flujo de Estados en Git

1. **Working Directory**: Archivos en edición.
2. **Staging Area**: Archivos preparados (`git add`).
3. **Repository**: Cambios guardados (`git commit`).

---

## 📸 Commits y HEAD

* **Commit:** Foto del proyecto:

  ```bash
  git commit -m "Descripción breve"
  ```
* **HEAD:** Puntero al último commit:

  ```bash
  git log -1
  git checkout <commit-id>  # Navegar a versión específica
  git checkout main         # Volver a main
  ```

---

## 🌿 Ramas y Merge

* **Crear rama:**

  ```bash
  git branch feature/nueva-funcionalidad
  ```
* **Cambiar de rama:**

  ```bash
  git checkout feature/nueva-funcionalidad
  ```
* **Fusionar (merge):**

  ```bash
  git checkout main
  git merge feature/nueva-funcionalidad
  ```

> **Conflictos:** Aparecen si dos cambios afectan la misma línea. Edita el archivo y usa `git add` para resolver.

---

## 🌐 GitHub Flow vs Gitflow

### GitHub Flow (ligero)

1. Trabaja en `main` o crea rama: `git checkout -b feature/x`
2. Commit y push: `git push -u origin feature/x`
3. Abre un Pull Request en GitHub
4. Revisa y mergea a `main`

### Gitflow (estructurado)

* `main`: Código de producción estable
* `develop`: Integración de features
* `feature/*`, `release/*`, `hotfix/*`

Comandos con Git Flow AVH:

```bash
git flow init
git flow feature start <nombre>
git flow feature finish <nombre>
```

(consulta más en: [https://github.com/petervanderdoes/gitflow-avh](https://github.com/petervanderdoes/gitflow-avh))

---

## 📦 Remotos y Sincronización

* **Listar remotos:** `git remote -v`
* **Agregar remoto:** `git remote add <alias> <URL>`
* **Eliminar remoto:** `git remote remove <alias>`
* **Sincronizar fork:**

  ```bash
  git remote add upstream <URL>
  git fetch upstream
  git rebase upstream/main
  git push origin main
  ```

---

## 📤 `git push` y 📥 `git pull`

| Comando                    | Acción                                        |
| -------------------------- | --------------------------------------------- |
| `git push origin <rama>`   | Envía commits al remoto                       |
| `git push --all origin`    | Envía todas las ramas                         |
| `git pull origin <rama>`   | Trae y fusiona cambios remotos                |
| `git pull --rebase origin` | Trae y reescribe tu historial sobre el remoto |

---

## ❗ Errores Comunes y Soluciones

| Problema                   | Solución                                          |
| -------------------------- | ------------------------------------------------- |
| Merge conflict no resuelto | Edita manualmente, luego `git add` + `git commit` |
| Push rechazado (rejected)  | `git pull --rebase` y luego `git push`            |
| HEAD detached              | `git checkout main` o `git checkout <rama>`       |

---

> ¡Así concluye tu guía de Git y GitHub! Practica estos comandos y flujos para dominar tus proyectos. 🚀
