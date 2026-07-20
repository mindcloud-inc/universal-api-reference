# Reset ID List Segment with Statsig

Resets an ID list segment in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/segments/{id}/id_list/reset`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Reset ID List Segment](https://docs.statsig.com/api-reference/segments/reset-id-list-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `ids` | body | `list` | yes | Request body field. |
