# Create Item with EasyContent

Creates a new content item in EasyContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapier/actions/create/create_an_item`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [Create Item](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | body | `number` | yes |
| `title` | body | `string` | yes |
| `description` | body | `string` | no |
| `keywords` | body | `string` | no |
| `templateId` | body | `number` | no |
| `categoryIds` | body | `list<number>` | no |
