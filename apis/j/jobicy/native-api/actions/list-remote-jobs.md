# List Remote Jobs with Jobicy

## Endpoint

- **Method:** `GET`
- **Path:** `/remote-jobs`
- **Base URL:** `https://jobicy.com/api/v2`
- **Official documentation:** [List Remote Jobs](https://jobicy.com/jobs-rss-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geo` | query | `string` | no | Optional Jobicy region slug such as usa, canada, europe, latam, apac, uk, germany, australia, or brazil. |
| `industry` | query | `string` | no | Optional Jobicy category slug such as engineering, devops, supporting, marketing, or finance. |
| `tag` | query | `string` | no | Optional keyword to search across job title and description. |
