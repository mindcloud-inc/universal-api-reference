# Remove IDs from Segment with Statsig

Removes IDs from a segment in Statsig.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/console/v1/segments/{id}/id_list`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Remove IDs from Segment](https://docs.statsig.com/api-reference/segments/remove-ids-from-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `ids` | body | `list` | yes | Request body field. |
