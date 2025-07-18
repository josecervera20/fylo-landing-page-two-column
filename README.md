# Frontend Mentor - Solución para Fylo landing page with two column layout ✨

Esta es una solución al desafío [Fylo landing page with two column layout challenge en Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-landing-page-with-two-column-layout-5ca5ef041e82137ec91a50f5). Los desafíos de Frontend Mentor te ayudan a mejorar tus habilidades de codificación construyendo proyectos realistas.

## Tabla de Contenidos 📋

- [Resumen](#resumen-📝)
  - [El desafío](#el-desafío)
  - [Captura de pantalla](#captura-de-pantalla-📸)
  - [Enlace](#enlace-🔗)
- [Mi Proceso](#mi-proceso-🚀)
  - [Construido con](#construido-con-🏗️)
  - [Lo que aprendí](#lo-que-aprendí-🧠)
  - [Desarrollo Continuo](#desarrollo-continuo-📈)
  - [Recursos Útiles](#recursos-útiles-📚)
- [Autor](#autor-🧑‍💻)
- [Agradecimientos](#agradecimientos-🙌)

## Resumen 📝

### El desafío

Los usuarios deberían ser capaces de:

- Ver el diseño óptimo para el sitio dependiendo del tamaño de la pantalla de su dispositivo.
- Ver los estados hover para todos los elementos interactivos en la página.

### Captura de pantalla 📸

![Captura de pantalla de la solución de Fylo landing page](./design/desktop-design.jpg)

### Enlace 🔗

- URL de la Solución (Repositorio): [https://github.com/josecervera20/fylo-landing-page-two-column](https://github.com/josecervera20/fylo-landing-page-two-column)

## Mi Proceso 🚀

### Construido con 🏗️

- Marcado semántico HTML5
- Propiedades personalizadas de CSS (Variables CSS)
- Flexbox (para layouts responsivos y alineación)
- Diseño Mobile-first
- [Google Fonts](https://fonts.google.com/specimen/Raleway) (Fuente Raleway)
- [Google Fonts](https://fonts.google.com/specimen/Open+Sans) (Fuente Open Sans)

### Lo que aprendí 🧠

Durante este proyecto, consolidé y profundicé en varias áreas clave del desarrollo frontend:

- **Diseño Responsivo con Flexbox**: Practiqué el uso extensivo de Flexbox para construir layouts adaptables a diferentes tamaños de pantalla, desde el diseño principal de las secciones hasta la alineación de elementos individuales. Esto me permitió organizar el contenido de manera flexible y robusta tanto en móvil como en escritorio.

  ```css
  /* Ejemplo de Flexbox para hero en desktop */
  @media (min-width: 768px) {
    .hero__main {
      display: flex;
      align-items: center;
      gap: 1.5em;
    }
    .hero__info {
      order: -1;
      text-align: left;
    }
  }

  /* Ejemplo de Flexbox para productive en desktop */
  @media (min-width: 768px) {
    .productive__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .productive__picture {
      width: 45%;
      order: 1;
    }
  }
  ```

- **Manejo de Backgrounds Complejos (`::before`)**: Implementé la imagen de fondo curvada utilizando un pseudo-elemento `::before` y `background-image`, que cambia entre la versión móvil y de escritorio con un `media query`. Esto demuestra un control preciso sobre elementos decorativos sin afectar la estructura HTML principal.

  ```css
  .hero::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100px;
    background-image: url("../images/bg-curve-mobile.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    left: 0;
    bottom: 0;
  }

  @media (min-width: 768px) {
    .hero::before {
      background-image: url("../images/bg-curve-desktop.svg");
    }
  }
  ```

- **Estados de Hover con Transiciones Suaves**: Apliqué efectos de hover a botones, enlaces y los iconos de redes sociales, utilizando transiciones para proporcionar una experiencia de usuario más pulida y reactiva.

  ```css
  .hero__input--cta:hover,
  .newsletter__submit:hover {
    background-color: hsl(224, 93%, 70%);
    cursor: pointer;
  }

  .productive__cta:hover {
    color: hsl(170, 45%, 60%);
    border-color: hsl(170, 45%, 60%);
    cursor: pointer;
  }

  .footer__media:hover {
    border-color: var(--moderate-cyan);
    transform: scale(1.1);
    cursor: pointer;
  }
  ```

- **Variables CSS para Consistencia**: Reforcé la práctica de definir variables CSS en `:root` para colores y fuentes, lo que hace el código más limpio, mantenible y fácil de escalar o modificar la paleta de colores globalmente.
  ```css
  :root {
    --very-dark-blue: hsl(243, 87%, 12%);
    --desaturated-blue: hsl(238, 22%, 44%);
    /* ... otras variables ... */
  }
  ```

### Desarrollo Continuo 📈

Me gustaría seguir profundizando en:

- **Validación de Formularios**: Implementar validaciones de formularios más robustas y con mejor feedback visual al usuario.
- **Accesibilidad (a11y)**: Prestar aún más atención a los atributos ARIA, la navegación con teclado y la semántica HTML para asegurar que mis proyectos sean accesibles para todos los usuarios.
- **Optimización del rendimiento**: Explorar técnicas avanzadas de optimización de imágenes (como `srcset` o formatos de nueva generación) y estrategias de carga para mejorar los tiempos de respuesta de la página.

### Recursos Útiles 📚

- [Frontend Mentor](https://www.frontendmentor.io/) - Una plataforma excelente para desafíos de codificación.
- [The Markdown Guide](https://www.markdownguide.org/) - Una referencia útil para la sintaxis de Markdown.
- [Devicons](https://www.google.com/search?q=https://devicons.github.io/) / [Twemoji](https://twemoji.twitter.com/) - Para añadir iconos a los READMEs.

## Autor 🧑‍💻

- GitHub - [@josecervera20](https://github.com/josecervera20)

## Agradecimientos 🙌

Agradezco a la comunidad de Frontend Mentor por proporcionar desafíos tan valiosos que me permiten mejorar mis habilidades y construir proyectos realistas.
