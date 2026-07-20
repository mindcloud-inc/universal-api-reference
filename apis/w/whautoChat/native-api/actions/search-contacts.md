# Search Contacts with WhautoChat

Finds contacts in WhautoChat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Search Contacts](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#1-search-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | query | `string` | no | Filter by tags |
| `workspaceId` | query | `string` | no | Filter by workspace |
| `channel` | query | `string` | no | Filter by channel |
| `searchText` | query | `string` | no | Free text search |
