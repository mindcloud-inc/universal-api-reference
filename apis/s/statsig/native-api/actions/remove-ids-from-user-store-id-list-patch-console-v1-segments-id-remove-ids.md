# Remove IDs from User Store ID List with Statsig

Removes IDs from a user store ID list in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/segments/{id}/remove_ids`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Remove IDs from User Store ID List](https://docs.statsig.com/api-reference/segments/remove-ids-from-user-store-id-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `ids` | body | `list` | yes | Request body field. |
| `version` | body | `number` | no | Request body field. |
