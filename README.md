# sds-documentation

This repository belongs to the Semantic Data Structuring Working Group (SDS WG) in the Open
Manufacturing Platform. It contains content to generate a joint SDS WG documentation across
different SDS WG repositories using Antora.

The documentation site is generated using Github actions and is available at
[https://openmanufacturingplatform.github.io/sds-documentation/](https://openmanufacturingplatform.github.io/sds-documentation/).

As of now, the Antora build for the website pulls the content from the following repositories and
sources:

- [SDS BAMM](https://github.com/OpenManufacturingPlatform/sds-bamm-aspect-meta-model/tree/main/src/docs)
- [SDS SDK](https://github.com/OpenManufacturingPlatform/sds-sdk/tree/main/documentation/developer-guide)

## Building locally

To build the documentation locally, you will need [Node.js](https://nodejs.org/en/) >=14. After
installing, run the following commands:

```sh
# Installs the Antora CLI and the site generator
npm i @antora/cli@2.3 antora-site-generator-lunr

# Runs Antora to generate the documentation
./node_modules/@antora/cli/bin/antora --fetch site.yml --generator antora-site-generator-lunr
```

After that, the documentation is available at `build/site/index.html`.
