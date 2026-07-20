# Add IDs to Segment with Statsig

Adds IDs to a segment in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/segments/{id}/id_list`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Add IDs to Segment](https://docs.statsig.com/api-reference/segments/add-ids-to-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `ids` | body | `list` | yes | Request body field. |
