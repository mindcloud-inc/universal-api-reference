# List Remote Jobs by Region with Jobicy

## Endpoint

- **Method:** `GET`
- **Path:** `/remote-jobs`
- **Base URL:** `https://jobicy.com/api/v2`
- **Official documentation:** [List Remote Jobs by Region](https://jobicy.com/jobs-rss-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geo` | query | `string` | yes | Jobicy region slug such as usa, canada, europe, latam, apac, uk, germany, australia, or brazil. |
