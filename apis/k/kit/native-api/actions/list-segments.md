# List Segments with Kit

Lists segments in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/segments`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Segments](https://developers.kit.com/api-reference/segments/list-segments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_total_count` | query | `boolean` | no | Set to true to include total_count in the response. Kit notes this can make the request slower. |
