# Create Segment with Statsig

Creates a segment in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/segments`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Segment](https://docs.statsig.com/api-reference/segments/create-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `id` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `type` | body | `string` | yes | Request body field. |
| `idType` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `creatorID` | body | `string` | no | Request body field. |
| `creatorEmail` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `rules` | body | `list` | no | Request body field. |
