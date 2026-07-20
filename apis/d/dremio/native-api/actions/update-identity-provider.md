# Update Identity Provider with Dremio

Updates an identity provider in Dremio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity-providers/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Identity Provider](https://docs.dremio.com/dremio-cloud/api/identity-providers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `provider` | body | `object` | yes |
