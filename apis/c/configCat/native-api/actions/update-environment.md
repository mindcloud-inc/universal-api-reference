# Update Environment with ConfigCat

Updates an existing environment in ConfigCat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/environments/:environmentId`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Update Environment](https://configcat.com/docs/api/reference/update-environment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | The identifier of the Environment. |
| `environment` | body | `object` | yes | Raw ConfigCat environment body. |
