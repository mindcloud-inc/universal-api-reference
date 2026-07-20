# Update Activation with KEYZY

Updates a license activation in KEYZY.

## Endpoint

- **Method:** `PUT`
- **Path:** `/activations/:id`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Update Activation](https://www.keyzy.io/docs/developers/rest-api/activations-put/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activated` | body | `boolean` | yes | Set to true or false. |
| `id` | path | `string` | yes | ID of the activation object. |
