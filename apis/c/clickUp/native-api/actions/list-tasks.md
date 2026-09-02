# List Tasks with ClickUp

Retrieves tasks from a specific ClickUp List.

## Endpoint

- **Method:** `GET`
- **Path:** `list/:list_id/task`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Tasks](https://developer.clickup.com/reference/gettasks)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | — |
| `custom_items` | query | `list<number>` | no | Send multiple values as a array. |
| `include_markdown_description` | query | `boolean` | no | — |
| `custom_fields` | query | `string` | no | — |
