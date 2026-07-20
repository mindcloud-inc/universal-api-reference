# Create Tag with Magileads

Creates a new tag in Magileads.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Create Tag](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The tag color in hex. |
| `name` | body | `string` | yes | The tag name. |
