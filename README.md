# 🎙️ Ariel Cáceres — humano digital (Frecuencia Bermejo IA)

Locutor digital de El Colorado, Formosa, que conversa en voz alta. Personaje ficticio creado con inteligencia artificial para la clase de Ética con IA («El Gran Juicio de la IA»).

## Archivos (van juntos en la misma carpeta)
| Archivo | Qué es |
|---|---|
| `index.html` | La página: foto animada, micrófono, voz y botones |
| `ariel-caceres.jpg` | La imagen base, sin modificar. Es obligatoria: la página la anima |

Agente de ElevenLabs: `agent_2601m7bqjwjgex59rjq4qrcjdznc` (identificador público, no es una clave secreta). Voz: «Tomás - Friendly High pitched Argentine», de la biblioteca pública (alegre, joven, argentina). Se cambia desde ElevenLabs sin tocar la página.

## Cómo funciona la animación
No es un modelo 3D: es **tu foto**, deformada en tiempo real. Rostro, ropa, fondo e iluminación son los de la imagen.
- **Boca y labios:** la mandíbula se abre y se cierra según la voz; el interior de la boca y los dientes aparecen al abrir. Los labios se redondean (sonidos tipo O/U) o se ensanchan (E/I) según el espectro del audio. Al terminar, vuelven a una posición cerrada.
- **Sincronización:** ElevenLabs no entrega visemas ni tiempos por palabra en este tipo de conexión, así que la boca sigue la **intensidad y el espectro del audio**. Es una sincronización **aproximada, no fonética exacta**.
- **Sin audio no hay habla:** si no suena la voz de Ariel, la boca queda cerrada.
- **Ojos:** parpadeo automático e independiente de la boca (siempre vuelve a ojos abiertos), con mirada al espectador y pequeños desvíos coordinados.
- **Expresiones:** atento al escuchar (cejas y leve inclinación), tranquilo al responder, sonrisa leve cuando hace humor.
- **Cabeza:** inclinaciones suaves; el fondo no se mueve.

## Publicar en GitHub Pages
1. Creá un repositorio (por ejemplo `ariel-caceres`) y subí `index.html` y `ariel-caceres.jpg` a la raíz.
2. **Settings → Pages → Deploy from a branch → `main` / `(root)` → Save**.
3. En un minuto queda en `https://TU-USUARIO.github.io/ariel-caceres/` (hace falta https para el micrófono).

## Guía de prueba
1. Abrí la página: Ariel parpadea, mira al frente y respira con pequeños movimientos.
2. Tocá **Hablar con Ariel** y aceptá el micrófono. Tiene que saludar una sola vez.
3. Mientras habla: la boca se abre y se cierra con la voz y no queda abierta en las pausas. Mientras lo escuchás a él, vos hablás: él queda atento.
4. Probá: «¿Quién sos?», «Contame un chiste», «¿Qué pasó con el audio viral de la emergencia hídrica?» (debe explicar la prueba técnica en una carpeta sin contraseña y la filtración de un tercero, reconocer su descuido y aclarar que nunca quiso provocar pánico).
5. **Finalizar conversación** corta la charla y la boca vuelve a reposo.

## Límites
- Al ser una foto, no admite giros grandes de cabeza ni gestos que no estén en la imagen (la sonrisa con dientes se cierra mediante deformación, no hay boca «nueva»).
- La calidad de la imagen (600 × 742 px) limita la nitidez en pantallas grandes.

## Estado
- Probado: sintaxis del código y que la deformación no se pliega ni da valores inválidos; las poses se revisaron sobre la foto en un prototipo.
- Agente creado en la cuenta de ElevenLabs con la voz alegre y el prompt basado en la ficha ética (el agente anterior no existía en esa cuenta).
- **Sin probar en un navegador real:** conexión con ElevenLabs, voz, micrófono y sincronización de la boca con el audio.
