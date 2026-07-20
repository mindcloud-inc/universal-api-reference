# List Remote Jobs by Category with Jobicy

## Endpoint

- **Method:** `GET`
- **Path:** `/remote-jobs`
- **Base URL:** `https://jobicy.com/api/v2`
- **Official documentation:** [List Remote Jobs by Category](https://jobicy.com/jobs-rss-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `industry` | query | `string` | yes | Jobicy category slug documented for the public feed, for example marketing or engineering. |
