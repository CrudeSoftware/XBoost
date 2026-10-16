# 🔒 Privacy Policy / Política de Privacidad

---

## 🇬🇧 English

### Data collected

XBoost **does NOT** collect personal data such as name, email, or passwords. But it DOES send the following to an external server:

**Sent to the server:**
- **Usernames of your X accounts** (extracted from `/account/switch`)
- **Page HTML** of the account selection page (to verify authentication)
- **Public stats** of users you follow (followers/following)
- **Follow completion notifications** (to update the system)

**Stored locally (chrome.storage.local):**
- Server session token
- Username of your connected account
- List of users you've already followed
- List of pending suggested users
- List of rejected users (unfavorable ratio)
- Auto-follow preference

**NOT collected:**
- ❌ Passwords
- ❌ X cookies
- ❌ X authentication tokens
- ❌ Private messages
- ❌ Browsing history

### Server

Requests go to a server whose domain is **resolved dynamically** after a redirect from `crudesoftware.github.io/X-Boost-Page/`. There is no publicly documented fixed URL to avoid blocking.

### Deleting your data

Uninstall the extension from `chrome://extensions`. This automatically deletes all `chrome.storage.local`.

To delete your server account, contact the developer (open an issue).

---

## 🇪🇸 Español

### Datos recopilados

XBoost **NO** recopila datos personales como nombre, email o contraseñas. Pero SÍ envía lo siguiente a un servidor externo:

**Enviado al servidor:**
- **Usernames de tus cuentas de X** (extraídos de `/account/switch`)
- **HTML de la página** de selección de cuentas (para verificar autenticación)
- **Estadísticas públicas** de usuarios que sigues (followers/following)
- **Notificaciones de follows completados** (para actualizar el sistema)

**Guardado localmente (chrome.storage.local):**
- Token de sesión del servidor
- Username de tu cuenta conectada
- Lista de usuarios que ya seguiste
- Lista de usuarios sugeridos pendientes
- Lista de usuarios rechazados (ratio desfavorable)
- Preferencia de auto-follow

**NO recopilados:**
- ❌ Contraseñas
- ❌ Cookies de X
- ❌ Tokens de autenticación de X
- ❌ Mensajes privados
- ❌ Historial de navegación

### Servidor

Las peticiones van a un servidor cuyo dominio se **resuelve dinámicamente** tras una redirección desde `crudesoftware.github.io/X-Boost-Page/`. No hay URL fija documentada públicamente para evitar bloqueos.

### Eliminar tus datos

Desinstala la extensión desde `chrome://extensions`. Esto borra automáticamente todo el `chrome.storage.local`.

Para borrar tu cuenta del servidor, contacta al desarrollador (abre un issue).
