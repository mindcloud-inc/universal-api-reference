# Update Client with Timelink

Updates an existing client in Timelink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/clients/:id`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Client](https://api.timelink.io/documentation#/Clients/patch_api_v1_clients__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
