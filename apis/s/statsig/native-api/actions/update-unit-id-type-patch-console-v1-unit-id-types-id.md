# Update Unit ID Type with Statsig

Updates a unit ID type in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/unit_id_types/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Unit ID Type](https://docs.statsig.com/api-reference/unit-id-types/update-unit-id-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `description` | body | `string` | yes | Request body field. |
