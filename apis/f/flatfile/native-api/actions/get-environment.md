# Get Environment with Flatfile

Retrieves a specific environment from Flatfile.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments/:environmentId`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Get Environment](https://reference.flatfile.com/api-reference/environments/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | Flatfile environment ID. Pass `current` to fetch the current environment. |
