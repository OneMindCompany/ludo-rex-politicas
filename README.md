# ludo-rex-politicas

Política de privacidad, términos de uso y borrado de cuenta **públicos** del juego **Ludo Rex**,
servidos con GitHub Pages:

> **https://onemindcompany.github.io/ludo-rex-politicas/** (política de privacidad)
>
> **https://onemindcompany.github.io/ludo-rex-politicas/terminos.html** (términos de uso)
>
> **https://onemindcompany.github.io/ludo-rex-politicas/eliminar-cuenta.html** (cómo borrar la cuenta)

Esas URL son las que declaran las fichas de Google Play y de la App Store, que exigen una política
accesible sin iniciar sesión y una dirección web para pedir el borrado de la cuenta, y las que abre
la app desde Ajustes.

## Fuente de verdad

Los textos canónicos viven en el repo privado `ludo-rex-docs`, en `publicacion/`:
`politica-de-privacidad.md` (espejo: `index.html`), `terminos-de-uso.md` (espejo: `terminos.html`)
y `eliminar-cuenta.md` (espejo: `eliminar-cuenta.html`). **Los cambios se hacen allá primero** y
estas páginas se actualizan como espejo, en el mismo cambio. Si divergen, la declaración pública
deja de coincidir con la interna, y eso es un problema legal.

## `app-ads.txt` no vive acá

AdMob busca `app-ads.txt` en la raíz del dominio del desarrollador,
`https://onemindcompany.github.io/app-ads.txt`, que sirve el repo `onemindcompany.github.io`
(el mismo de Suscripción). Este repo es un sitio de proyecto y se sirve bajo `/ludo-rex-politicas/`.

## Desviación del estándar de repositorios

**Es público**, como `suscripcion-politicas`: su única razón de existir es que las tiendas y los
jugadores puedan leerlo. No contiene código del juego, que sigue privado.

## Ramas

| Rama | Rol | Protegida |
|---|---|---|
| `main` | Publicado: GitHub Pages sirve desde acá | ✅ |
| `qa` | Validación | ✅ |
| `develop` | Integración del trabajo en curso | ✅ |
| `feature/*` | Trabajo puntual, se integra a `develop` vía PR | ❌ |

Flujo: `feature/*` → `develop` → `qa` → `main`, siempre por pull request (rulesets
`protect-main`/`protect-qa`/`protect-develop`, sin bypass). Un cambio de política no está publicado
hasta que llega a `main`. Ciclo de trabajo: skill `control-de-versiones-onemind`.
