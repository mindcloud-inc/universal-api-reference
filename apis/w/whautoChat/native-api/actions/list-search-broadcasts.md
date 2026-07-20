# List/Search Broadcasts with WhautoChat

Finds broadcasts in WhautoChat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/broadcasts`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [List/Search Broadcasts](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#1-listsearch-broadcasts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | no | Filter by workspace ID |
| `endDate` | query | `date` | no | Filter by end date |
| `searchText` | query | `string` | no | Free text search |
