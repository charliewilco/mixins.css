# Mixins.css

Curated set of handy CSS mixins in the `@apply` syntax with more to come. The [`@apply` specification](http://tabatkins.github.io/specs/css-apply-rule/) is in motion and under a [feature flag in Chrome](https://www.chromestatus.com/feature/5753701012602880).

```css
:root {
  --visually-hidden: {
    position: absolute;
    width: 1px;
    height: 1px;
    overflow: hidden;
    top: 0;
    clip: rect(1px, 1px, 1px, 1px);
  }

  --clearfix: {
    content: "";
    display: table;
    clear: both;
  }

  --position-zero: {
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
  }
}
```

## Install

```sh
npm i -S mixins.css
```

## Usage

```css
.Grid {
  @apply --clearfix;
}

.Module {
  @apply --visually-hidden;
}
```

## PostCSS

If you want to compile these down with PostCSS there's a couple great plugins [postcss-apply](https://github.com/pascalduez/postcss-apply) and that plugin is also bundled in with [cssnext](https://github.com/moox/postcss-cssnext).
