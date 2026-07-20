# Get IDs in a Segment with Statsig

Retrieves segment IDs from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/segments/{id}/id_list`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get IDs in a Segment](https://docs.statsig.com/api-reference/segments/get-ids-in-a-segment)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
