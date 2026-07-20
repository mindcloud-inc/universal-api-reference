# Update Tag with Statsig

Updates a tag in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/tags/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Tag](https://docs.statsig.com/api-reference/tags/update-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `isCore` | body | `boolean` | no | Request body field. |
