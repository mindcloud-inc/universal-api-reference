# List Project Categories with EasyContent

Retrieves categories from a selected EasyContent project.

## Endpoint

- **Method:** `GET`
- **Path:** `/zapier/resources/categories`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [List Project Categories](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `projectId` | query | `number` | yes |
