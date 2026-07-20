# Get Page Stats with Simple Analytics

Retrieves stats for a specific page in Simple Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{hostname}}/{{pagePath}}.json`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Get Page Stats](https://docs.simpleanalytics.com/api/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | path | `string` | yes | Website hostname to query, for example `simpleanalytics.com`. |
| `pagePath` | path | `string` | yes | Path segment without the `.json` suffix, for example `contact` or `blog/my-post`. |
| `start` | query | `string` | no | Start date or placeholder such as `yesterday`. |
| `end` | query | `string` | no | End date or placeholder such as `today`. |
| `fields` | query | `string` | no | Comma-separated stats fields such as `pageviews,visitors`. |
