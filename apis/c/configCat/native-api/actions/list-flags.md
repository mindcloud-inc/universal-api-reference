# List Flags with ConfigCat

Retrieves flags from a ConfigCat config.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/configs/:configId/settings`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [List Flags](https://configcat.com/docs/api/reference/get-settings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | path | `string` | yes | The identifier of the Config. |
