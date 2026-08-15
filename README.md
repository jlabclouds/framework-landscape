- add [pluto.land](https://pluto.land) for free pluto notebooks hosting
- [Strelka](https://github.com/target/strelka-ui?tab=readme-ov-file)

Real-time file scanning at enterprise scale.

# Framework Landscape

This project uses the Landscape2 toolchain to render a local static site from the YAML configuration files.

## Run locally

From the project root, install the CLI if needed:

```bash
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/cncf/landscape2/releases/download/v1.1.0/landscape2-installer.sh | sh
```

Build the landscape:

```bash
landscape2 build \
  --data-file data.yml \
  --settings-file settings.yml \
  --guide-file guide.yml \
  --logos-path logos \
  --output-dir build
```

Serve the generated site locally:

```bash
landscape2 serve --landscape-dir build
```

Then open the URL shown by the server (usually http://127.0.0.1:8000) in your browser.

## Files

- data.yml: main landscape content
- guide.yml: category and subcategory descriptions
- settings.yml: site settings and group configuration
- logos/: logo assets used by the landscape
