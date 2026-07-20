# List Remote Jobs by Region and Category with Jobicy

## Endpoint

- **Method:** `GET`
- **Path:** `/remote-jobs`
- **Base URL:** `https://jobicy.com/api/v2`
- **Official documentation:** [List Remote Jobs by Region and Category](https://jobicy.com/jobs-rss-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geo` | query | `string` | yes | Jobicy region slug such as usa, canada, europe, or latam. |
| `industry` | query | `string` | yes | Jobicy category slug documented for the public feed, for example marketing or engineering. |
