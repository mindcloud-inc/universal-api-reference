# Count Crypto News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/crypto/count`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [Count Crypto News](https://newsdata.io/documentation#count-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Start date for crypto count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
| `interval` | query | `string` | no | Grouping interval for count results. |
| `q` | query | `string` | no | Keyword or phrase used for crypto count estimation. |
| `to_date` | query | `string` | yes | End date for crypto count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
