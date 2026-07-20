# List/Search Staff with WhautoChat

Finds staff members in WhautoChat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/staffs`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [List/Search Staff](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/staff/#1-listsearch-staff)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | no | Filter by workspace ID |
| `searchText` | query | `string` | no | Free text search |
