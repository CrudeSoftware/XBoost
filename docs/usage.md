🎮 Usage Guide / Guía de Uso

Complete walkthrough of XBoost — from first launch to daily use.

Guía completa de XBoost — desde el primer inicio hasta el uso diario.

---

🇬🇧 English

Table of Contents

1. First Launch
2. Device Verification
3. Connecting Your Account
4. Understanding the Popup
5. Following Users
6. Auto-Follow Mode
7. Submitting Your Account
8. The On-Page Banner
9. Follow-Back Badges
10. Troubleshooting

---

1. First Launch

After installing the extension (see Install on PC or Install on Android), you'll see the XBoost icon in your browser toolbar.

How to open the popup:

· PC: Click the XBoost icon in the toolbar
· Android: Menu (⋮) → Extensions → XBoost

../images/pc/08-popup-open.png

On first launch, you'll see a loading screen:

🔄 "Verifying device..."

This is normal. Wait a few seconds for the process to complete.

---

2. Device Verification

XBoost performs a brief verification step before showing the main interface.

Duration: 5–15 seconds typically.

If it fails:

· You'll see "Could not connect to server"
· A Retry button appears
· Check your internet connection and try again

../images/pc/08-popup-open.png

⚠️ Note: Some antivirus software or corporate firewalls may interfere with this step. If verification fails repeatedly, temporarily disable your antivirus and try again.

---

3. Connecting Your Account

Once the device is verified, you'll see the Connect Your X Account screen.

../images/pc/08-popup-open.png

Steps:

1. Click "Connect account"
2. A new tab opens at x.com/account/switch
3. If you're not logged in, log in first
4. Your accounts are detected automatically
5. The tab closes and you're verified

What the extension reads:

· The list of your X usernames (from the account switcher)
· Public metadata of the page (to confirm you're authenticated)

What it does NOT read:

· ❌ Your password
· ❌ Your session cookies
· ❌ Your private messages

📖 See PRIVACY.md for full details.

If it fails:

· "No accounts found" → Make sure you're logged into X
· "Verification failed" → Refresh x.com and try again
· "Session expired" → Close and reopen the extension

---

4. Understanding the Popup

Once verified, the popup shows:

```
┌────────────────────────────────────┐
│  XBOOST              [Auto: ON/OFF]│
├────────────────────────────────────┤
│  ┌──────────────────────────────┐  │
│  │      [BANNER ZONE]           │  │
│  │  (dynamic HTML from server)  │  │
│  └──────────────────────────────┘  │
├────────────────────────────────────┤
│  [Submit your account for review]  │
├────────────────────────────────────┤
│  Suggested to follow               │
│  Follow them and they'll follow... │
│                                    │
│  [Follow all]                      │
│                                    │
│  ┌──────────────────────────────┐  │
│  │  User card 1                 │  │
│  │  @username — 1.2K followers  │  │
│  │                  [Follow]    │  │
│  └──────────────────────────────┘  │
│  ┌──────────────────────────────┐  │
│  │  User card 2                 │  │
│  │  @username — 850 followers   │  │
│  │                  [Follow]    │  │
│  └──────────────────────────────┘  │
│  ...                               │
└────────────────────────────────────┘
```

Sections:

Section Purpose
Auto toggle Enables/disables automatic following
Banner zone Dynamic content, updates every 30s
Submit button Sends your account for review
Follow list Suggested users to follow
Follow all Follows every user in the list

---

5. Following Users

Follow a single user

1. Find a user card in the list
2. Click the Follow button
3. A hidden tab opens x.com/username
4. The extension checks the user's stats:
   · If followers * 0.7 < following → follows
   · Otherwise → skips (adds to rejected list)
5. The tab closes automatically
6. The user disappears from your list
7. A toast confirms: "Followed @username"

Time per follow: ~2–4 seconds.

Follow all users

1. Click "Follow all" at the top of the list
2. The button becomes "Stop" (red)
3. Progress shows as X/Y on the button
4. Each user is followed one by one with a 2-second delay
5. When done, a toast shows: "Followed N users"

To cancel: Click the red Stop button at any time.

⚠️ Rate limits: X has strict rate limits. Following too many users too fast may trigger a temporary block. The 2-second delay helps, but use Follow all responsibly.

---

6. Auto-Follow Mode

The Auto toggle at the top of the popup enables automatic following.

When enabled:

· Every 5 seconds, the extension polls the server for new users
· If new eligible users appear, they're followed automatically
· No manual interaction needed

When disabled:

· New users still appear in the list
· You must click Follow or Follow all manually

Recommendation: Leave it off unless you're actively growing your account. Auto-follow increases the risk of X detecting automation.

../images/pc/07-extension-installed.png

---

7. Submitting Your Account

The "Submit your account for review" button adds your account to the pool that other users see.

How it works:

1. Click the button
2. The extension sends your username to the server
3. The server validates it
4. If approved, you'll appear in other users' follow lists
5. Other users will follow you → you gain followers

Status messages:

Message Meaning
✓ Account validated! You're now visible to other users
✗ Failed to submit Server rejected the request
Not verified You need to verify your account first

Requirements:

· Your account must be verified (Step 3)
· Your account must meet the server's eligibility criteria (public, active, not suspended)

---

8. The On-Page Banner

When you visit x.com/home or x.com/notifications, XBoost injects a custom banner at the top of your timeline.

../images/pc/08-popup-open.png

Features:

· Fetched from the server every 30 seconds
· Displays announcements, tips, or promotions
· Adapts to light/dark themes
· Disappears when you leave those pages

If the banner fails to load:

· You'll see a ⚠️ icon with "Banner unavailable"
· This is usually temporary — it retries automatically

---

9. Follow-Back Badges

When you open x.com/notifications, users who followed you back are highlighted with a badge:

🎉 Thanks for following back — followed via XBoost

../images/pc/08-popup-open.png

How it works:

1. XBoost scans notification cards every 15 seconds
2. When it finds "followed you" + "te siguió" text
3. It checks if you followed that user via XBoost
4. If yes, adds the badge

Purpose: Encourages reciprocity and shows the system is working.

---

10. Troubleshooting

Extension won't load

Problem Solution
Icon doesn't appear Pin it from the extensions menu 🧩
Popup blank Reload the extension from chrome://extensions
"Manifest missing" You selected the wrong folder during install

Verification fails

Problem Solution
"Verifying device..." stuck Check internet; disable VPN/antivirus temporarily
"Could not connect to server" Retry; the server may be temporarily down
"Session expired" Close and reopen the popup

Account connection fails

Problem Solution
"No accounts found" Log into x.com first
Page closes too fast Disable other X extensions temporarily
"Account access issue" X may have blocked automation — wait 24h

Following doesn't work

Problem Solution
Button does nothing Check that you're verified
"Failed to follow" User may be private or suspended
Only some users followed Normal — only those meeting the ratio criteria are followed

Rate limit warnings

If X shows "Too many requests" or "Rate limit exceeded":

1. Stop all XBoost activity
2. Wait 15–30 minutes
3. Try again with fewer follows
4. Consider disabling auto-follow

⚠️ Repeated rate limit violations can lead to account suspension. Use responsibly.

Token expired

If you see "Session expired. Please verify again."

1. Close the popup
2. Reopen it
3. Click "Connect account" again
4. Your previous followed list is preserved

---

Best Practices

✅ Do:

· Follow 20–50 users per day maximum
· Keep auto-follow off unless actively growing
· Take breaks between sessions
· Use a secondary account if you're worried about your main one
· Check the PRIVACY.md to understand what's sent

❌ Don't:

· Follow hundreds of users in one session
· Leave auto-follow running 24/7
· Use it on an account you can't afford to lose
· Ignore rate limit warnings

---

🇪🇸 Español

Índice

1. Primer inicio
2. Verificación del dispositivo
3. Conectar tu cuenta
4. Entender el popup
5. Seguir usuarios
6. Modo auto-follow
7. Enviar tu cuenta
8. El banner en la página
9. Badges de follow-back
10. Solución de problemas

---

1. Primer inicio

Después de instalar la extensión (ver Instalación en PC o Instalación en Android), verás el icono de XBoost en la barra de herramientas.

Cómo abrir el popup:

· PC: Clic en el icono de XBoost en la barra
· Android: Menú (⋮) → Extensiones → XBoost

../images/pc/08-popup-open.png

En el primer inicio verás una pantalla de carga:

🔄 "Verifying device..."

Esto es normal. Espera unos segundos a que termine el proceso.

---

2. Verificación del dispositivo

XBoost realiza una breve verificación antes de mostrar la interfaz principal.

Duración: 5–15 segundos típicamente.

Si falla:

· Verás "Could not connect to server"
· Aparece un botón Retry
· Verifica tu conexión a internet e intenta de nuevo

../images/pc/08-popup-open.png

⚠️ Nota: Algunos antivirus o firewalls corporativos pueden interferir con este paso. Si la verificación falla repetidamente, desactiva temporalmente tu antivirus e intenta de nuevo.

---

3. Conectar tu cuenta

Una vez verificado el dispositivo, verás la pantalla Connect Your X Account.

../images/pc/08-popup-open.png

Pasos:

1. Pulsa "Connect account"
2. Se abre una nueva pestaña en x.com/account/switch
3. Si no has iniciado sesión, hazlo primero
4. Tus cuentas se detectan automáticamente
5. La pestaña se cierra y quedas verificado

Qué lee la extensión:

· La lista de usernames de tus cuentas de X
· Metadatos públicos de la página (para confirmar autenticación)

Qué NO lee:

· ❌ Tu contraseña
· ❌ Tus cookies de sesión
· ❌ Tus mensajes privados

📖 Ver PRIVACY.md para más detalles.

Si falla:

· "No accounts found" → Asegúrate de estar logueado en X
· "Verification failed" → Refresca x.com e intenta de nuevo
· "Session expired" → Cierra y reabre la extensión

---

4. Entender el popup

Una vez verificado, el popup muestra:

```
┌────────────────────────────────────┐
│  XBOOST              [Auto: ON/OFF]│
├────────────────────────────────────┤
│  ┌──────────────────────────────┐  │
│  │      [ZONA DE BANNER]        │  │
│  │  (HTML dinámico del servidor)│  │
│  └──────────────────────────────┘  │
├────────────────────────────────────┤
│  [Enviar mi cuenta para revisión]  │
├────────────────────────────────────┤
│  Sugeridos para seguir             │
│  Síguelos y te seguirán de vuelta  │
│                                    │
│  [Seguir todos]                    │
│                                    │
│  ┌──────────────────────────────┐  │
│  │  Tarjeta usuario 1           │  │
│  │  @usuario — 1.2K seguidores  │  │
│  │                  [Seguir]    │  │
│  └──────────────────────────────┘  │
│  ┌──────────────────────────────┐  │
│  │  Tarjeta usuario 2           │  │
│  │  @usuario — 850 seguidores   │  │
│  │                  [Seguir]    │  │
│  └──────────────────────────────┘  │
│  ...                               │
└────────────────────────────────────┘
```

Secciones:

Sección Propósito
Toggle Auto Activa/desactiva el seguimiento automático
Zona banner Contenido dinámico, se actualiza cada 30s
Botón Submit Envía tu cuenta para revisión
Lista de follows Usuarios sugeridos para seguir
Seguir todos Sigue a todos los usuarios de la lista

---

5. Seguir usuarios

Seguir a un usuario individual

1. Encuentra una tarjeta de usuario en la lista
2. Pulsa el botón Seguir
3. Se abre una pestaña oculta en x.com/usuario
4. La extensión comprueba las estadísticas del usuario:
   · Si seguidores * 0.7 < siguiendo → lo sigue
   · Si no → lo omite (lo añade a la lista de rechazados)
5. La pestaña se cierra automáticamente
6. El usuario desaparece de tu lista
7. Un toast confirma: "Followed @usuario"

Tiempo por follow: ~2–4 segundos.

Seguir a todos

1. Pulsa "Seguir todos" arriba de la lista
2. El botón se convierte en "Stop" (rojo)
3. El progreso se muestra como X/Y en el botón
4. Cada usuario se sigue uno por uno con un delay de 2 segundos
5. Al terminar, un toast muestra: "Followed N users"

Para cancelar: Pulsa el botón rojo Stop en cualquier momento.

⚠️ Rate limits: X tiene límites estrictos. Seguir demasiados usuarios muy rápido puede provocar un bloqueo temporal. El delay de 2 segundos ayuda, pero usa Seguir todos con responsabilidad.

---

6. Modo auto-follow

El toggle Auto en la parte superior del popup activa el seguimiento automático.

Cuando está activado:

· Cada 5 segundos la extensión consulta al servidor por nuevos usuarios
· Si aparecen nuevos usuarios elegibles, los sigue automáticamente
· Sin interacción manual

Cuando está desactivado:

· Los nuevos usuarios siguen apareciendo en la lista
· Debes pulsar Seguir o Seguir todos manualmente

Recomendación: Déjalo apagado a menos que estés creciendo activamente. Auto-follow aumenta el riesgo de que X detecte la automatización.

../images/pc/07-extension-installed.png

---

7. Enviar tu cuenta

El botón "Enviar mi cuenta para revisión" añade tu cuenta al pool que ven los demás usuarios.

Cómo funciona:

1. Pulsa el botón
2. La extensión envía tu username al servidor
3. El servidor lo valida
4. Si es aprobado, aparecerás en las listas de otros usuarios
5. Otros usuarios te seguirán → ganas seguidores

Mensajes de estado:

Mensaje Significado
✓ ¡Cuenta validada! Ahora eres visible a otros usuarios
✗ Error al enviar El servidor rechazó la solicitud
No verificado Necesitas verificar tu cuenta primero

Requisitos:

· Tu cuenta debe estar verificada (Paso 3)
· Debe cumplir los criterios del servidor (pública, activa, no suspendida)

---

8. El banner en la página

Cuando visitas x.com/home o x.com/notifications, XBoost inyecta un banner personalizado en la parte superior de tu timeline.

../images/pc/08-popup-open.png

Características:

· Se obtiene del servidor cada 30 segundos
· Muestra anuncios, consejos o promociones
· Se adapta a temas claros/oscuros
· Desaparece al salir de esas páginas

Si el banner falla:

· Verás un ⚠️ con "Banner unavailable"
· Normalmente es temporal — reintenta automáticamente

---

9. Badges de follow-back

Cuando abres x.com/notifications, los usuarios que te siguieron de vuelta se resaltan con un badge:

🎉 Gracias por seguir de vuelta — seguido vía XBoost

../images/pc/08-popup-open.png

Cómo funciona:

1. XBoost escanea las tarjetas de notificación cada 15 segundos
2. Cuando encuentra "followed you" + "te siguió"
3. Comprueba si tú seguiste a ese usuario vía XBoost
4. Si sí, añade el badge

Propósito: Fomentar la reciprocidad y mostrar que el sistema funciona.

---

10. Solución de problemas

La extensión no carga

Problema Solución
El icono no aparece Fíjalo desde el menú de extensiones 🧩
Popup en blanco Recarga la extensión desde chrome://extensions
"Manifest missing" Seleccionaste la carpeta incorrecta al instalar

La verificación falla

Problema Solución
"Verifying device..." atascado Verifica internet; desactiva VPN/antivirus temporalmente
"Could not connect to server" Reintenta; el servidor puede estar caído
"Session expired" Cierra y reabre el popup

La conexión de cuenta falla

Problema Solución
"No accounts found" Inicia sesión en x.com primero
La página se cierra muy rápido Desactiva otras extensiones de X temporalmente
"Account access issue" X puede haber bloqueado la automatización — espera 24h

El follow no funciona

Problema Solución
El botón no hace nada Verifica que estás verificado
"Failed to follow" El usuario puede ser privado o estar suspendido
Solo se siguen algunos Normal — solo se siguen los que cumplen el criterio de ratio

Avisos de rate limit

Si X muestra "Too many requests" o "Rate limit exceeded":

1. Detén toda actividad de XBoost
2. Espera 15–30 minutos
3. Intenta de nuevo con menos follows
4. Considera desactivar el auto-follow

⚠️ Violaciones repetidas del rate limit pueden llevar a suspensión de cuenta. Úsalo con responsabilidad.

Token expirado

Si ves "Session expired. Please verify again."

1. Cierra el popup
2. Reábrelo
3. Pulsa "Conectar cuenta" de nuevo
4. Tu lista de seguidos se conserva

---

Buenas prácticas

✅ Sí:

· Sigue 20–50 usuarios por día como máximo
· Mantén el auto-follow apagado salvo que estés creciendo activamente
· Toma descansos entre sesiones
· Usa una cuenta secundaria si te preocupa perder la principal
· Lee PRIVACY.md para entender qué se envía

❌ No:

· Sigas cientos de usuarios en una sola sesión
· Dejes el auto-follow encendido 24/7
· Lo uses en una cuenta que no puedas permitirte perder
· Ignores los avisos de rate limit
