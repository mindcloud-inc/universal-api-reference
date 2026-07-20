# List/Search Segments with WhautoChat

Finds segments in WhautoChat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/segments`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [List/Search Segments](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#1-listsearch-segments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | no | Filter by workspace ID |
| `searchText` | query | `string` | no | Free text search |
