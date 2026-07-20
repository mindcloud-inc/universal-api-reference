# List Assets with ServiceTrade

Retrieves all assets from ServiceTrade.

## Endpoint

- **Method:** `GET`
- **Path:** `asset`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [List Assets](https://api.servicetrade.com/api/docs#resource-asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAfter` | query | `number` | yes | Unix timestamp filter required by ServiceTrade for asset list queries in this scaffold. |
