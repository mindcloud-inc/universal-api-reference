# Add IDs to User Store ID List with Statsig

Adds IDs to a user store ID list in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/segments/{id}/add_ids`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Add IDs to User Store ID List](https://docs.statsig.com/api-reference/segments/add-ids-to-user-store-id-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `ids` | body | `list` | yes | Request body field. |
| `version` | body | `number` | no | Request body field. |
