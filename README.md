# ODS Document Generation Service

A document generation service that transforms document templates in a remote Bitbucket repository into PDF documents.

## Distribute

```
./gradlew shadowJar
```

## Run

```
./gradlew run
```

## Test

```
./gradlew test
```

## Document Templates

When processing a template `type` at a specific `version`, and data into a document, the service expects the Bitbucket repository to have a `release/${version}` branch that contains the template type at `/templates/${type}.html.tmpl`.

## Requirements

### Packages

- [wkhtmltopdf](https://wkhtmltopdf.org/)

### Environment

- `BITBUCKET_URL`
- `BITBUCKET_USERNAME`
- `BITBUCKET_PASSWORD`
- `BITBUCKET_DOCUMENT_TEMPLATES_PROJECT`
- `BITBUCKET_DOCUMENT_TEMPLATES_REPO`

## Reference

This project is based on https://github.com/jooby-project/gradle-starter.
