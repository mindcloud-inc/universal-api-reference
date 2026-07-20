# Search Contacts with Go4Clients

Finds contacts in Go4Clients by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/groupscontacts/contacts/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Search Contacts](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchFilters` | query | `string` | yes | JSON array of filter objects with key, type, and value. |
