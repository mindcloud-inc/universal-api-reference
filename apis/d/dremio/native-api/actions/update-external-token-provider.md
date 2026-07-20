# Update External Token Provider with Dremio

Updates an external token provider in Dremio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/external-token-providers/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update External Token Provider](https://docs.dremio.com/dremio-cloud/api/external-token-providers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `provider` | body | `object` | yes |
