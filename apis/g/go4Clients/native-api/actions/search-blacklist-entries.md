# Search Blacklist Entries with Go4Clients

Finds blacklist entries in Go4Clients by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/blacklist/v1.0/`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Search Blacklist Entries](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchFilters` | query | `string` | yes | JSON object of blacklist filters. |
| `pagingInformation` | query | `string` | no | JSON object with start and limit. |
