# Update Source Tag with Chatsistant

Updates an existing source tag in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/source-tag/:uuid/update`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Update Source Tag](https://docs.chatsistant.com/api-reference/source-tags/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The source tag color. |
| `name` | body | `string` | no | The source tag name. |
| `uuid` | path | `string` | no | The tag UUID. |
