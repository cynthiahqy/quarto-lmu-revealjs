# quarto-lmu-revealjs

Reveal.js format with LMU Munich styling (LMU green, Roboto-friendly, LMU logo, 1280×720, chalkboard).

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

## Notes

- Colours are set in `_extensions/lmu/lmu-revealjs.scss` with `!default`, so a project `_brand.yml` takes precedence.
- Logos in `_extensions/lmu/logos/`; change with `logo:` in the YAML.
- Fonts (Roboto) come from the project's `_brand.yml`; the extension does not load them.
