# Create Item with GatherContent

Creates a new item in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/items`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Create Item](https://docs.gathercontent.com/reference/createitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uuid` | body | `string` | yes | Destination folder UUID. |
| `project_id` | path | `string` | yes | Project id. |
| `template_id` | body | `string` | no | Template ID to attach. |
