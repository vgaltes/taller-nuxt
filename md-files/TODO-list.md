# TODO taller

[x] Pantallazos 2018 en resumen: reducir tamaño

[x] Pasos instalación en README (algo similar a [Django Girls](https://tutorial.djangogirls.org/es/installation/) o [VueVixens](https://vuevixens.github.io/docs/workshop/ch1.html)):
- [x] Crear cuenta GitHub si no se tiene (para Codesandbox y para despliegue).
- [x] Opción 1: Descargar en local
    - [x] [Nuxt (node, npm, npx) en Mac, Windows y Linux](https://nuxtjs.org/guide/installation/).
    - [x] Vue Dev tools en Chrome.
    - [x] VS Code.
    - [x] Git.
- [x] Opción 2: Usar [Codesandbox](https://codesandbox.io/s/github/nuxt/codesandbox-nuxt)
- [x] Spotify API.

[x] Rama "nuxt0": Conectar con API Spotify para ver qué pantallas se podrían mostrar en la aplicación.
- [x] Crear un Client ID en el [Dashboard](https://developer.spotify.com/dashboard/applications):
    - App Name: Wecodefy
    - Description: Get your statistics from last year in a similar way as spotify wrappers.
    - What are you building? Website.
    - Are you developing a commercial integration? No
- [x] Get Top User artists: Se necesita [User Authorization](https://developer.spotify.com/documentation/general/guides/authorization-guide/): To get that authorization, your application generates a call to the Spotify Accounts Service /authorize endpoint, passing along a list of the scopes for which access permission is sought.
    - [Get User's Top Artists and Tracks](https://developer.spotify.com/console/get-current-user-top-artists-and-tracks/?type=artists&time_range=&limit=&offset=)
- [x] Implicit Grant: [Example](https://gist.github.com/igorPhelype/68239ecab9afcc50230ce0c61c3bac2f), [Authorization Guide](https://developer.spotify.com/documentation/general/guides/authorization-guide/).

[ ] Rama en GitHub por cada funcionalidad de la aplicación (nuxt1, ...nuxtn):
- [x] Rama "nuxt2": Rama inicial con las dependencias necesarias para la aplicación.
- [ ] Rama "nuxt2": Componentes y layout con parte estática. Global CSS (metodología BEM). Nuxt-link. Transición entre páginas. SEO y meta tags. Mostrar code-splitting.
    - [x] Imagen Wecodefy: Transparente.
    - [x] Prueba de estructura del layout.
    - [x] Global CSS.
    - [x] Header y footer con elementos opcionales: Crear cada página y añadir condiciones en el layout.
    - [x] Nuxt-link para moverse entre páginas (ver todos los botones)
    - [ ] Separar TheFooter en 3 componentes para separar funcionalidad.
    - [ ] Maquetación de cada página con metodología BEM y usando Flexbox.
    - [ ] Añadir SEO y meta tags. ¿Dónde añadir el título de la página?
    - [ ] Mostrar code-splitting.
    - [ ] Probar los linters de JS y CSS.
    - [ ] Apuntar en README todos los pasos a partir de layout.
- [ ] Rama "nuxt3: Spotify API. Plugins ¿cuál?. Vuex guardar estado distintas páginas.
- [ ] Rama "nuxt4": Ver código generado estático en dist con el pre rendering. Despliegue estático GitHub Pages o Netlify. 

[ ] Hacer la misma aplicación en Codesandbox para apuntar los pasos en README.
    - Crear cuenta en [CodeSandbox](https://codesandbox.io/) y hacer un fork de [codesandbox-nuxt](https://codesandbox.io/s/github/nuxt/codesandbox-nuxt).

[ ] Explicación Nuxt en README:
- [ ] Qué es Nuxt: framework Vue. SEO friendly. Mejora performance.
- [ ] Modos Pre-render y SSR. 
- [ ] Muestra en Chrome Dev tools de parte de SEO y code-splitting.
- [ ] Lo que no vamos a ver (en cursos de Nuxt en Vue School): 
    - [ ] Async data / fetch. 
    - [ ] Dynamic routes. 
    - [ ] Despliegue Heroku.
 
[ ] Enlace a la demo en GitHub Pages para mostrar en el taller (local con VueDevTools y GitHub Pages sin VueDevTools).

[ ] Revisar versión final del README de master, debería contener lo último (rama nuxtn)

## Opcional

[ ] ¿Usar nuxt-linter?

[ ] ¿Proxy para API?

[ ] Animaciones CSS entre páginas

## Despliegue

- Añadir en el Dashboard de spotify la redirect uris de producción.

## Día del taller

[ ] Versión en local del repo + en 1 usb + GitHub.