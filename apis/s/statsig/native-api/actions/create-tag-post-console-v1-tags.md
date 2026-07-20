# Create Tag with Statsig

Creates a tag in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/tags`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Tag](https://docs.statsig.com/api-reference/tags/create-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `isCore` | body | `boolean` | no | Request body field. |
