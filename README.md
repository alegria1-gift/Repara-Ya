# Repara Ya

Proyecto web basado en Servitec Álvarez, con el nombre y la paleta visual de Repara Ya.

## Paleta
- Principal: `#18005e`
- Secundario: `#de932a`
- Fondo: `#e6dede`

## Estructura
- `index.html`: página principal.
- `script.js`: interacción del formulario y envío a `/api/enviar`.
- `api/enviar.js`: función de Vercel que envía los correos con Resend.
- `css/estilos.css`: hoja de estilos conservada del proyecto original.

## Variables de entorno en Vercel
Configura estas variables en el proyecto nuevo:
- `RESEND_API_KEY`: API Key privada de Resend.
- `DESTINO_EMAIL`: correo que recibirá las solicitudes.
- `REMITENTE_EMAIL`: remitente verificado/autorizado en Resend (para pruebas, `onboarding@resend.dev`, sujeto a las restricciones de la cuenta gratuita).

Después de crear o modificar variables, realiza un nuevo despliegue.

## Despliegue
1. Crea un repositorio nuevo llamado `repara-ya`.
2. Sube el contenido de esta carpeta a la raíz del repositorio (no subas la carpeta contenedora como un nivel extra).
3. Importa el repositorio en Vercel.
4. Añade las tres variables de entorno en Vercel.
5. Despliega y prueba el formulario. Revisa los registros de la función `/api/enviar` si hay errores.

**Seguridad:** nunca pongas `RESEND_API_KEY` en `index.html`, `script.js` ni en el repositorio.


## Actualización visual

La página utiliza una identidad visual para servicio técnico:
- Azul profundo `#18005E`: confianza y tecnología.
- Naranja `#DE932A`: energía y botones de acción.
- Gris claro `#F4F5F8`: fondo limpio.
- Blanco `#FFFFFF`: tarjetas y formularios.

La hoja de estilos se encuentra en `css/estilos.css`. El formulario conserva el envío mediante `api/enviar.js` y Resend. Para que el correo funcione, configura las variables de entorno `RESEND_API_KEY`, `DESTINO_EMAIL` y `REMITENTE_EMAIL` en el hosting.
