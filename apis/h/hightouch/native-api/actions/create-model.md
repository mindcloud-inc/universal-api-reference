# Create Model with Hightouch

Creates a new model in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/models`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Model](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skipColumnQuery` | query | `boolean` | no | Whether to skip querying columns while creating the model. |
| `name` | body | `string` | yes | The model name. |
| `slug` | body | `string` | yes | The model slug. |
| `queryType` | body | `string` | yes | The model query type. |
| `sourceId` | body | `number` | yes | The source ID the model is connected to. |
| `isSchema` | body | `boolean` | yes | Whether the model is only used to build other models. |
| `primaryKey` | body | `string` | yes | The primary key for synced query results. |
