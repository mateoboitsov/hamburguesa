# la burger

una hero page animada construida con humano + ia. el resultado de lo que pasa cuando alguien diseña bien y le pide a la ia que lo ejecute.

→ [ver en vivo](#) <!-- añade tu url de deploy aquí -->

---

## qué hay aquí

- hamburguesa que se desencaja al hacer scroll, capa a capa
- texto con efecto flicker + scramble (las letras se revuelven antes de aparecer)
- títulos que emergen de abajo con máscara
- etiquetas de ingredientes que aparecen y desaparecen según el scroll
- marquee continuo en la siguiente sección
- menú animado que desliza desde la derecha
- adaptado a móvil

---

## cómo usarlo

```bash
git clone https://github.com/mateoboitsov/hamburguesa.git
cd hamburguesa
pnpm install
pnpm dev
```

si no tienes pnpm:

```bash
npm install -g pnpm
```

---

## stack

| herramienta | para qué |
|-------------|----------|
| React + Vite | base del proyecto |
| GSAP + SplitText | todas las animaciones de texto |
| ScrollTrigger | animaciones vinculadas al scroll |
| Lenis | smooth scroll |

---

## cómo se construyó

1. imagen de la hamburguesa generada con ChatGPT
2. cada ingrediente recortado en Figma en frames de la misma anchura
3. diseño de la hero en Figma con referencias visuales buscadas antes
4. exportado a React con Builder.io
5. a partir de ahí, todo con IA: animaciones, scroll, menú, responsive

el truco de la hamburguesa: todos los frames tienen la misma anchura y la altura se ajusta para que el `margin-bottom` negativo sea igual en todos — así la imagen encogida se ve perfecta.

---

## estructura

```
src/
├── components/
│   ├── AnimatedText.jsx   # line reveal reutilizable
│   ├── Menu.jsx           # menú con animación de entrada
│   └── Menu.css
├── pages/
│   ├── HeroPage.jsx       # toda la lógica de animaciones
│   └── HeroPage.css
└── main.jsx               # lenis + gsap ticker
```

---

*esto es el 5% de lo que ocurre cuando un humano y una ia deciden hacer algo bonito juntos.*
*los humanos de [maibo](https://maibo.es) + ia · 2026*
