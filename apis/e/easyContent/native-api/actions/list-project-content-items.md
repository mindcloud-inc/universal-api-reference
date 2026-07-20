# List Project Content Items with EasyContent

Retrieves content items from a selected EasyContent project.

## Endpoint

- **Method:** `GET`
- **Path:** `/zapier/resources/articles`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [List Project Content Items](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `projectId` | query | `number` | yes |
