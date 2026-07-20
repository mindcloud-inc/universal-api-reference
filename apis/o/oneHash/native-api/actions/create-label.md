# Create Label with OneHash

Creates a new label in OneHash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/accounts/:accountId/labels`
- **Base URL:** `https://chat.onehash.ai`
- **Official documentation:** [Create Label](https://developers.chatwoot.com/api-reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | OneHash Chat account id. |
| `color` | body | `string` | no | Hex color. |
| `description` | body | `string` | no | Label description. |
| `show_on_sidebar` | body | `string` | no | Whether the label appears in the sidebar. |
| `title` | body | `string` | no | Label title. |
