# Search Atlas Clusters with Satori Cyber

Finds Atlas clusters in Satori Cyber.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/authorization-analytics/search-atlas-clusters`
- **Base URL:** `https://app.satoricyber.com`
- **Official documentation:** [Search Atlas Clusters](https://app.satoricyber.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | Satori account ID for authorization analytics scope. |
| `search` | query | `string` | no | Optional search string for atlas cluster matching. |
