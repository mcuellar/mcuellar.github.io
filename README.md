# mcuellar.github.io
Personal website and professional profile for Gaston Marcelo Cuellar, built with MkDocs and deployed via GitHub Pages at mcuellar.github.io. This site showcases my background, projects, and interests in a clean, responsive format.

## Features

- Comprehensive documentation for cloud and development technologies
- Beautiful Material Design theme with dark/light mode
- Full-text search functionality
- Responsive design for mobile and desktop
- Easy navigation with top navigation tabs

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/mcuellar/cloud-docs-hub.git
cd cloud-docs-hub
```

### 2. Set Up Virtual Environment

#### On macOS/Linux:

```bash
# Create virtual environment
python3 -m venv .venv

# Activate virtual environment
source .venv/bin/activate
```

#### On Windows:

```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run MkDocs Locally

```bash
# Start the development server
mkdocs serve

# Optional. If auto-reload not working
mkdocs serve --livereload
```

The documentation site will be available at `http://127.0.0.1:8000/`

The development server features:

- Auto-reload when you make changes to documentation files
- Live preview of your edits
- Fast rebuild times

## Building the Documentation

To build the static site for deployment:

```bash
mkdocs build
```

This will create a `site/` directory with the static HTML files.

## Project Structure

```
cloud-docs-hub/
├── docs/                      # Documentation source files
│   ├── index.md              # Home page
│   ├── resume.md            # Resume
│   ├── project.md            # Projects
├── mkdocs.yml                # MkDocs configuration file
├── requirements.txt          # Python dependencies
└── README.md                # This file
```


## Adding New Documentation

1. Create a new Markdown file in the appropriate directory under `docs/`
2. Update `mkdocs.yml` to include the new page in the navigation
3. The changes will be reflected immediately if you're running `mkdocs serve`

Example:

```yaml
nav:
  - Home: index.md
  - AWS:
      - Overview: aws/index.md
      - EC2 Guide: aws/ec2.md  # New page
```

## Customization

### Changing Theme Colors

Edit the `theme.palette` section in `mkdocs.yml`:

```yaml
theme:
  palette:
    - scheme: default
      primary: indigo  # Change this
      accent: indigo   # Change this
```

### Adding Extensions

MkDocs supports various Markdown extensions. Add them in `mkdocs.yml`:

```yaml
markdown_extensions:
  - your_extension_here
```

## Deployment

### GitHub Pages

To deploy to GitHub Pages:

```bash
mkdocs gh-deploy --force
```

This command builds the documentation and pushes it to the `gh-pages` branch.

## Deactivating Virtual Environment

When you're done working:

```bash
deactivate
```

## Troubleshooting

### Port Already in Use

If port 8000 is already in use, specify a different port:

```bash
mkdocs serve -a localhost:8001
```

### Module Not Found

Make sure you've activated the virtual environment and installed dependencies:

```bash
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

## Additional Resources

- [MkDocs Documentation](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org/)

## License

This project is open source and available for use in documentation and educational purposes.
