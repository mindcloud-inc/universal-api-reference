# List Archived News with NewsData.io

## Endpoint

- **Method:** `GET`
- **Path:** `/archive`
- **Base URL:** `https://newsdata.io/api/1`
- **Official documentation:** [List Archived News](https://newsdata.io/documentation#news-archive)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Category filter for archived news results. |
| `country` | query | `string` | no | Country code filter for archived news results. |
| `from_date` | query | `string` | no | Start date for archived news retrieval. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
| `language` | query | `string` | no | Language code filter for archived news results. |
| `q` | query | `string` | no | Keyword or phrase to search for in archived news results. |
| `to_date` | query | `string` | no | End date for archived news retrieval. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. |
