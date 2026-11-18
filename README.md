# App socias CEAGA

Prototipo web de la app para las empresas socias de CEAGA, con su backoffice. Proyecto del COP (LEINN) con CEAGA como cliente.

- **Web (demo):** https://ceaga-app.vercel.app
- **Versión para presentar (30 de 40 funciones):** https://ceaga-app.vercel.app/?version=demo
- **Repo:** https://github.com/iriavintia/ceaga-app

## Qué hay hoy

- `index.html`: la app completa en un solo archivo (HTML estático, React desde CDN). No necesita compilación ni `npm`.
- Despliegue: Vercel, como sitio estático (sin framework y sin build).
- La demo tiene **dos vistas** (barra de arriba): *App de socias* y *Backoffice CEAGA*. Lo que hace una socia en la app aparece en el backoffice.
- **Versión para presentar:** con `?version=demo` en la dirección se ocultan las funciones 5, 9, 13, 15, 19, 21, 23, 26, 31 y 33 de la lista de funciones. Sin el parámetro se ve todo. Para cambiar qué se oculta, edita la lista `OCULTAS_EN_DEMO` al principio del script de `index.html`.
- Los datos son **de ejemplo** y se reinician al recargar la página. Nada se guarda.

Pantallas de la demo: Para ti, Agenda (eventos, detalle e inscripción, networking, encuesta), Ecosistema (empresas y ficha de empresa), Recursos, Mi espacio y Registro.

## Piloto (hasta el 11/12)

Lo acordado de palabra con CEAGA el 13/11. **Pendiente de que CEAGA lo confirme por escrito.**

Formato: **web app** (se puede «añadir a la pantalla de inicio»), no app de tienda.

### Qué incluye

| Pieza | Qué es | Dónde está en el código |
|---|---|---|
| Eventos | Calendario, detalle del evento e inscripción | `Agenda`, `DetalleEvento`, `Inscripcion` |
| Networking dentro de los eventos | Aparecer en el networking de un evento y pedir reuniones | `Networking` |
| Ficha de empresa | Ficha de empresa del catálogo de CEAGA | `Ecosistema`, `DetalleEmpresa` |
| CEAGA Info | Noticias y novedades de CEAGA dentro de la app | `Actualidad` |
| Prueba | Probarlo con las 19 personas de CEAGA antes de abrirlo a las empresas | n/a |

### Qué queda fuera (de momento)

- Para ti, Recursos, Mi espacio, KAM/CAM, ayudas e informes: están en la demo, pero no entran en el piloto.
- Marketplace: sin definir qué es ni qué se espera ver.
- Backoffice completo: el piloto necesita lo mínimo para cargar eventos e información. El de 6 áreas queda para después.

### Por confirmar con CEAGA

- Quién carga CEAGA Info y los eventos, y en qué formato.
- Evento real y grupo de 10-15 personas para probar.
- Catálogo de empresas: exportación o vista incrustada, y quién lo actualiza.
- Asignaciones de CAM por empresa (la demo lo llama KAM; falta confirmar la sigla).

### Fechas

- 18/11: CEAGA confirma alcance y respuestas.
- 4/12 (o antes): reunión de validación con CEAGA.
- 11/12: cierre del reto.

## Cómo trabajar

1. Clona el repo y abre `index.html` en el navegador. No hay nada que instalar.
2. **Una rama por persona** (`nombre/tema`). No se sube directamente a `main` salvo cosas mínimas.
3. Cambios pequeños y claros; cada commit dice qué cambia.
4. Antes de subir, abre la demo en local y comprueba que no se ha roto la app ni el backoffice.
5. Vercel publica la web. Falta confirmar si se despliega solo al subir a `main` (?).

## Reglas de datos

- **El repo es público.** No subas datos reales de CEAGA, de socias ni de clientes, ni claves, ni contraseñas ni tokens.
- Los archivos `.env*` ya están en `.gitignore`.
- Para el piloto con datos reales habrá que pasar el repo a privado y decidir dónde viven los datos. Está por decidir.

## Pendiente técnico

- [ ] Dar permiso de escritura a los cinco del equipo.
- [ ] Pasar el repo a privado antes de meter datos reales.
- [ ] Cuenta de Vercel con un correo del equipo, para no depender de una sola persona.
- [ ] Repartir el piloto en piezas con responsable (la tabla de arriba es la base).
- [ ] Decidir cómo se cargan eventos e información de CEAGA (a mano en el backoffice o desde los datos de CEAGA).
