# Count Market News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/market/count`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [Count Market News](https://newsdata.io/documentation#count-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Start date for market count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
| `interval` | query | `string` | no | Grouping interval for count results. |
| `q` | query | `string` | no | Keyword or phrase used for market count estimation. |
| `to_date` | query | `string` | yes | End date for market count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
