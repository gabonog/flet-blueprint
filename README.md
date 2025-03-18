[//]: # (Copyright 2025 Gabriel Nogueira)
[//]: # (Licensed under the Apache License, Version 2.0 \(the "License"\);)
[//]: # (you may not use this file except in compliance with the License.)
[//]: # (You may obtain a copy of the License at)
[//]: # (http://www.apache.org/licenses/LICENSE-2.0)

# Flet Blueprint

## Project file structure

```
README.md
docker-compose-devel.yaml          # Docker Compose file for the development environment
flet/
├── Dockerfile                     # Dockerfile to build the application image
└── app/
    ├── README.md                  # General information about the application
    ├── uv.lock                    # Dependency lock file
    ├── .gitignore                 # Files and folders to ignore in Git
    ├── .python-version            # Python version for the environment
    ├── .pyproject.toml            # Project configuration (e.g., with Poetry)
    ├── .venv/                     # Virtual environment (generated)
    └── src/
        ├── main.py                # Application entry point
        ├── assets/                # Static resources
        │   └── fonts/             # Fonts and other typography files
        ├── models/                # Data model definitions
        ├── services/              # Business logic and application services
        ├── storage/               # Storage management
        │   ├── data/              # Persistent data
        │   └── temp/              # Temporary files
        ├── tests/                 # Unit and integration tests
        ├── ui/                    # User interface
        │   ├── components/        # Reusable UI components (e.g., appbar, navbar)
        │   │   ├── appbar.py
        │   │   └── navbar.py
        │   ├── theme/             # Themes and visual styles
        │   └── views/             # Views or screens of the application
        │       └── home.py
        └── utils/                 # Utility and helper functions
            ├── __init__.py        # Optional: re-export common functions if desired
            ├── config.py          # Global configurations and constants
            ├── exceptions.py      # Custom exceptions
            ├── decorators.py      # Decorators (e.g., @view to register views)
            ├── loaders.py         # Functions for dynamic resource loading (views, modules, templates, etc.)
            ├── helpers.py         # General helper functions (formatting, date handling, etc.)
            ├── registry.py        # Global registry (e.g., mapping routes to views)
            └── logger.py          # Logging configuration (optional)
```
