<a href="https://photon-platform.net/">
    <img src="https://photon-platform.net/user/images/photon-logo-banner.png" alt="photon" title="photon" align="right" height="120" />
</a>


# photon ✴ Species

## 0.1.0

---


> templates for species

- [configuration](#configuration)
- [templates](#templates)
- [scaffolds](#scaffolds)
- [scss](#scss)
- [assets](#assets)
- [languages](#languages)

# configuration
blueprints.yaml

fields:
- enabled
- built_in_css
- built_in_js

Before configuring this plugin, you should copy the `user/plugins/photon-species/photon-species.yaml` to `user/config/plugins/photon-species.yaml` and only edit that copy.

Here is the default configuration and an explanation of available options:

```yaml
enabled: true
built_in_css: true
built_in_js: true

description: Custom Text added by the **photon-species** plugin (disable plugin to remove)
```

Note that if you use the admin plugin, a file with your configuration, and named photon-species.yaml will be saved in the `user/config/plugins/` folder once the configuration is saved in the admin.


# blueprints

```sh
blueprints
├── family.yaml
├── genus.yaml
└── species.yaml
```

### Family
family.yaml
extends: article
fields:
- features
  - header.species.description

### Species
species.yaml
extends: article
fields:
- header.data.species
  - .commonName
  - .scientificName
  - .commonFamilyName
  - .scientificFamilyName
  - .habitat
  - .floweringStart
  - .floweringEnd
  - .gardenLocation
  - .nativeTo
  - .datePlanted

### Genus
genus.yaml
extends: article
fields:
- features
  - header.species.description

# templates

```sh
templates
├── _articles
│   └── _block
├── _json-ld
│   └── species.html.twig
├── family.html.twig
├── genus.html.twig
└── species.html.twig
```

# scss

```sh
scss
├── articles
│   └── _species.scss
├── templates
│   └── _species.scss
└── species.scss
```

# assets

```sh
assets
├── species.css
├── species.css.map
└── species.js
```

# languages

```sh
languages
└── en.yaml
```


## Installation

- all photon plugins are installed as git submodules. More on that later.



## Configuration


## Usage

Select template type when creating a new page

## Credits


## To Do

- [ ] Future plans, if any


copyright &copy; 2020
