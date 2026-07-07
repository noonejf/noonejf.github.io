# Cómo publicar todo (una sola vez, ~10 minutos)

Todo está commiteado localmente. Solo falta crear los repos en GitHub y hacer push.
Necesitas estar logueado en github.com como **noonejf**.

## 1. Portafolio → https://noonejf.github.io (gratis, sin dominio)

1. En GitHub: **New repository** → nombre exactamente `noonejf.github.io` → público → **sin** README inicial.
2. En PowerShell:
   ```powershell
   cd C:\Users\jf19s\Desktop\PROYECTOS\ACTUALES\PORTFOLIO
   git remote add origin https://github.com/noonejf/noonejf.github.io.git
   git push -u origin main
   ```
3. Espera ~1 minuto. Tu página queda viva en **https://noonejf.github.io**.
   (GitHub Pages se activa solo para repos con ese nombre.)

## 2. README de perfil (la portada de tu GitHub)

1. **New repository** → nombre exactamente `noonejf` → público → marca **Add a README**.
2. Reemplaza su contenido con el de `github-profile/README.md` de esta carpeta
   (puedes editarlo directo en la web de GitHub y pegar).
3. Tu perfil github.com/noonejf ahora muestra proyectos, stack y stats.

## 3. Repo del control PID (LAB2)

1. **New repository** → nombre sugerido `servo-pid-control` → público → sin README.
2. ```powershell
   cd C:\Users\jf19s\Desktop\PROYECTOS\ANTIGUOS\SISTEMAS_DE_CONTROL\LAB2
   git remote add origin https://github.com/noonejf/servo-pid-control.git
   git push -u origin main
   ```

## 4. V_HAND (ya existe en tu GitHub)

El README nuevo y el .gitignore ya están commiteados en tu rama `JoSeSi`:
```powershell
cd C:\Users\jf19s\Desktop\PROYECTOS\ANTIGUOS\V_HAND_INTERFACE
git push
```
Si el repo es privado y quieres lucirlo: Settings → Danger Zone → **Change visibility → Public**.
(Tienes cambios locales sin commitear en `Comunicacion_maestro.py` y `requirements.txt` — revísalos tú antes de commitear.)

## 5. Toques finales en GitHub (2 min, mucho impacto visual)

- En cada repo: ⚙️ junto a "About" → agrega **descripción** y **topics**
  (ej. `robotics`, `pyqt5`, `control-systems`, `matlab`, `embedded`).
- En `noonejf.github.io` → About → website: `https://noonejf.github.io`.
- En tu perfil → Edit profile → website: `https://noonejf.github.io`.
- Fija (Pin) los 4 repos en tu perfil.

## Mantenimiento

- **CVs**: edita los `.tex` en `PROYECTOS\DATA_ME`, corre `.\compilar.ps1`,
  copia los PDFs nuevos a `PORTFOLIO\cv\` y haz `git add . ; git commit -m "update cv" ; git push`.
- **Portafolio**: edita `index.html`, commit y push — se publica solo.
