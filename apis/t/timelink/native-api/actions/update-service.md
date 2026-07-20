# Update Service with Timelink

Updates an existing service in Timelink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/services/:id`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Service](https://api.timelink.io/documentation#/Services/patch_api_v1_services__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
