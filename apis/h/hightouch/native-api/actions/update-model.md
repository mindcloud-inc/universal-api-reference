# Update Model with Hightouch

Updates an existing model in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/models/{modelId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Model](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `number` | yes | The model ID. |
| `name` | body | `string` | no | The model name. |
| `primaryKey` | body | `string` | no | The primary key for synced query results. |
| `isSchema` | body | `boolean` | no | Whether the model is only used to build other models. |
