# Create Flag with ConfigCat

Creates a new flag in ConfigCat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/configs/:configId/settings`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Create Flag](https://configcat.com/docs/api/reference/create-setting/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | path | `string` | yes | The identifier of the Config. |
| `flag` | body | `object` | yes | Raw ConfigCat flag body. Create requires key, name, and settingType. |
