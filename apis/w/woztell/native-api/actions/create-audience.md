# Create Audience with Woztell

Creates an audience in your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Create Audience](https://doc.woztell.com/open-api-reference/#mutation-createAudience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.name` | body | `string` | no | Audience name. |
| `variables.input.description` | body | `string` | no | Audience description. |
| `variables.input.static` | body | `boolean` | no | Whether the audience is static. |
| `variables.input.tags` | body | `list<string>` | no | Tags to assign to the audience. Send multiple values as a array. |
