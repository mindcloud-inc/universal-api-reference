# Get Course Details Localized with Teachlr Organizations

## Endpoint

- **Method:** `GET`
- **Path:** `/courses-online/:slug`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Get Course Details Localized](https://soporte.teachlr.com/base-de-conocimientos/como-obtener-los-detalles-de-un-curso-de-una-escuela-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Slug of the course to retrieve. |
| `lang` | query | `string` | yes | ISO 639-1 language code to localize category and subcategory labels. |
