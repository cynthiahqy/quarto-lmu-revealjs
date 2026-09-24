# quarto-lmu-revealjs

Reveal.js format with LMU Munich styling (LMU green, 1280×720, slide numbers, fade transition).

## Install

```bash
quarto add cynthiahqy/quarto-lmu-revealjs
```

## Use

```yaml
format: lmu-revealjs
```

Any Reveal.js option can be overridden as usual, e.g.

```yaml
format:
  lmu-revealjs:
    footer: "https://example.org"
    incremental: true
```

## Not included

Teaching-specific options (`chalkboard`, `smaller`, `code-line-numbers`, `execute:` settings) are left to the project; see [quarto-lmu-subject-template](https://github.com/cynthiahqy/quarto-lmu-subject-template) for an example.

## Notes

- Colours are set in `_extensions/lmu/lmu-revealjs.scss` with `!default`, so a project `_brand.yml` takes precedence.
- **Logo:** the extension ships logos in `_extensions/lmu/logos/` but does not set one by default. Quarto resolves an extension's `logo:` incorrectly in websites that use `_brand.yml` (broken `../../_extensions/...` path), so set the logo in the project instead:

  ```yaml
  # _brand.yml (recommended for projects with a brand file)
  logo:
    small: _extensions/lmu/logos/LMU_Logo_RGB_InvertiertGruen.png
  ```

  In a website with a green navbar, `_brand.yml`'s logo also appears in the navbar, where the green logo is invisible. Use `LMU_Logo_RGB_InvertiertWeiss.png` there and set a separate slide logo with `logo:` in the deck or shared YAML (e.g. `_slides.yml`).

  For a standalone document with no `_brand.yml`, `logo: _extensions/lmu/logos/LMU_Logo_RGB_InvertiertGruen.png` in the YAML.
- Fonts (Roboto) come from the project's `_brand.yml`; the extension does not load them.
