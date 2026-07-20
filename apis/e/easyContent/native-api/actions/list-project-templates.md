# List Project Templates with EasyContent

Retrieves templates from a selected EasyContent project.

## Endpoint

- **Method:** `GET`
- **Path:** `/zapier/resources/templates`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [List Project Templates](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `projectId` | query | `number` | yes |
