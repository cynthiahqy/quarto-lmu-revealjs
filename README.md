# quarto-lmu-revealjs

Reveal.js format with LMU Munich styling (LMU green, LMU logo, 1280×720, slide numbers, fade transition).

## Install

```bash
quarto add soda-lmu/quarto-lmu-revealjs
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

Teaching-specific options (`chalkboard`, `smaller`, `code-line-numbers`, `execute:` settings) are left to the project; see [quarto-lmu-subject-template](https://github.com/soda-lmu/quarto-lmu-subject-template) for an example.

## Notes

- Colours are set in `_extensions/lmu/lmu-revealjs.scss` with `!default`, so a project `_brand.yml` takes precedence.
- Logos in `_extensions/lmu/logos/`; change with `logo:` in the YAML.
- Fonts (Roboto) come from the project's `_brand.yml`; the extension does not load them.
