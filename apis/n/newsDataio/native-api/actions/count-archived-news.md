# Count Archived News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/count`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [Count Archived News](https://newsdata.io/documentation#count-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Start date for archive count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
| `interval` | query | `string` | no | Grouping interval for count results. |
| `q` | query | `string` | no | Keyword or phrase used for archive count estimation. |
| `to_date` | query | `string` | yes | End date for archive count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
