# Update Config with ConfigCat

Updates an existing config in ConfigCat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/configs/:configId`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Update Config](https://configcat.com/docs/api/reference/update-config/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | path | `string` | yes | The identifier of the Config. |
| `config` | body | `object` | yes | Raw ConfigCat config body. |
