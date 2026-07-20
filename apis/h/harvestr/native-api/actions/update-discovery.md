# Update Discovery with Harvestr.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/discovery/{id}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Update Discovery](https://developers.harvestr.io/api/update-a-discovery/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `discoveryStateId` | body | `string` | no | The discovery state ID to set |
