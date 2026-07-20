# List Courses By Category And Subcategory with Teachlr Organizations

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/available`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [List Courses By Category And Subcategory](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | yes | Slug of the course category to filter by. |
| `subcategory` | query | `string` | yes | Slug of the course subcategory to filter by. |
