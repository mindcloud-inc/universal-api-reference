# Update Webset with Exa

Updates an existing webset in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/websets/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Update Webset](https://exa.ai/docs/websets/api/websets/update-a-webset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id or externalId of the Webset |
| `metadata` | body | `object` | no | Set of key-value pairs you want to associate with this object. |
