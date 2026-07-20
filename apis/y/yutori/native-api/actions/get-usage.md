# Get Usage with Yutori

Retrieves Yutori account usage, active scouts, and rate limits.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/usage`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Get Usage](https://docs.yutori.com/reference/usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Usage window to return: 24h, 7d, 30d, or 90d. |
