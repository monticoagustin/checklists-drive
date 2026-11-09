# checklists-drive (3dF + sync con Google Drive)
- Repo: https://github.com/monticoagustin/checklists-drive (copia propia; origen: monticof-commits/Checklists-Drive @ c363bc6).
- Destino: https://teskel.online/3df/ (Space Teskel, path `3df/`). Pages original: https://monticof-commits.github.io/Checklists-Drive/
- Siempre debe cumplir las normas ISO. No agregar nada que las rompa; no inventar normas.
- Identidad 3dF: Archivo, negro/blanco, logo 3dF, sin neumorfismo. No copiar branding de otros proyectos.
- Google Drive: el Client ID actual es de otro proyecto de Google Cloud y solo acepta localhost:8765 y monticof-commits.github.io. Para que ande en teskel.online hay que agregar `https://teskel.online` como origen autorizado (ver SETUP-GOOGLE.md) o usar un Client ID propio.
- Rutas relativas, sin service worker: funciona bajo cualquier subpath.
- Git: commits locales libres; `git push` SOLO cuando el usuario lo pida.
