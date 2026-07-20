# List Links with Linkly

Retrieves links from Linkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspace_id/list_links`
- **Base URL:** `https://app.linklyhq.com/api/v1`
- **Official documentation:** [List Links](https://linklyhq.com/support/link-shortening-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search query to filter links. |
