# Get Webset with Exa

Retrieves a webset from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/websets/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Webset](https://exa.ai/docs/websets/api/websets/get-a-webset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id or externalId of the Webset. |
| `expand[]` | query | `array<string>` | no | Expand the response with the specified resources |
