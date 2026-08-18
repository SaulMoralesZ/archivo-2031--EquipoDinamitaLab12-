| Hallazgo | Dónde estaba | Técnica de Git | Comando exacto | Referencia |
|---|---|---|---|---|
| FRAG-01 | Archivo eliminado de la rama principal de la cinta | Buscar eliminaciones y leer el archivo desde el commit anterior | `git log refs/cinta/heads/main --diff-filter=D --name-status --oneline` / `git show 0ad3603^:bitacora/frag-01.txt` | `0ad3603^` |
| FRAG-02 | Mensaje de la etiqueta anotada de respaldo | Inspeccionar directamente el objeto tag | `git cat-file -p refs/cinta/tags/respaldo/pre-incidente` | `refs/cinta/tags/respaldo/pre-incidente` |
| Glifo | Commit apuntado por la etiqueta de respaldo | Leer un archivo desde el commit referenciado por el tag | `git show 'refs/cinta/tags/respaldo/pre-incidente^{}:assets/sello.svg'` | `9a771852cdc176c42cbbe3e1c5619620ea5432c9` |
