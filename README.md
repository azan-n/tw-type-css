# tw-type-css

A collection of Tailwind CSS v4.0 utilities with typographic primitives. Unlike the all-or-nothing reliance on `prose` in `@tailwind/typography`, this plugin offers both primitives and a `tw-prose` utility.

This package is a replacement for [`@tailwindcss/typography`][Original_Plugin_GitHub]. It embraces the new [CSS-first architecture][TailwindCSS_Custom_Utilities], providing a pure CSS solution without relying on the legacy JavaScript plugin system. Furthermore, unlike the original plugin, this plugin does not make color choices for you.

## Usage
1. Install the package with `npm`
    ```sh
    npm install -D tw-type-css
    ```
2. Add the following line to your root CSS file 
    ```css
   @import "tw-animate-css";
    ```
3. Start using the utilities
    ```html
    <article class="tw-prose">
      <h1>Garlic bread with cheese: What the science tells us</h1>
      <p>
        For years parents have espoused the health benefits of eating garlic bread with cheese to their
        children, with the food earning such an iconic status in our culture that kids will often dress
        up as warm, cheesy loaf for Halloween.
      </p>
      <p>
        But a recent study shows that the celebrated appetizer may be linked to a series of rabies cases
        springing up around the country.
      </p>
      <!-- ... -->
    </article>
    ```
    Utility classes `text-{100,200,300,400,500,600,700,800,900,1000}`, `leading-{160,150,130,120,110,100}`, `tracking-{003,002,001,000}`, `font-weight-{300,400,500,700}`. `heading-{1-5}` and `body-{base,lg,sm}` allow using the same type scale without having to use `tw-prose`. Consider the following example that attempts to use semantic HTML while still conforming to the defined type scale.
    
    ```html
    <h1 class="heading-3">Heading that shouldn't be as large as an h1 but should be an h1 for semantics</h1>
    ```

This plugin assumes fonts are defined in the tailwind default `--font-mono`, `--font-sans` variables. Furthermore, this plugin uses `--spacing()` utilities to align with the base project.

## Customization
The plugin simple rules to generate font sizes for the type scale, and percentage based measures for line height. The font sizes are controlled by the  `--tw-type-scale-ratio` (defaults to 1.25 Major Scale) and `--tw-type-scale-base` (defaults to 1 rem). It is possible to change the overall size and variance in size by controlling these two.

[Original_Plugin_GitHub]: https://github.com/tailwindlabs/tailwindcss-typography
[TailwindCSS_Custom_Utilities]: https://tailwindcss.com/docs/adding-custom-styles#adding-custom-utilities
