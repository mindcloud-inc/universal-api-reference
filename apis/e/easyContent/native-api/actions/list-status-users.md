# List Status Users with EasyContent

Retrieves users assignable to a selected EasyContent workflow status.

## Endpoint

- **Method:** `GET`
- **Path:** `/zapier/resources/users-that-can-be-assigned-to-status`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [List Status Users](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `projectId` | query | `number` | yes |
| `statusId` | query | `number` | yes |
