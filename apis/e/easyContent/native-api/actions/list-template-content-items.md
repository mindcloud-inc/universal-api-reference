# List Template Content Items with EasyContent

Retrieves EasyContent items that use a specific template.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/content/templates/:templateId/content-items`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [List Template Content Items](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | path | `number` | yes |
| `title` | query | `string` | no |
