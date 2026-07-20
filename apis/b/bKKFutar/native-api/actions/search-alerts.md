# Search Alerts with BKK Futar

Finds active alerts in BKK Futar by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/search.json`
- **Base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`
- **Official documentation:** [Search Alerts](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#search-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query matched against alert title, description, or identifier. |
| `start` | query | `number` | no | Start of the search interval in epoch seconds. |
| `end` | query | `number` | no | End of the search interval in epoch seconds. |
| `minResult` | query | `number` | no | Minimum number of elements returned. |
| `includeReferences` | query | `string` | no | Reference data to include in the response. |
