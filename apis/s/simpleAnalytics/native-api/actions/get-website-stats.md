# Get Website Stats with Simple Analytics

Retrieves aggregated website stats from Simple Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{hostname}}.json`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Get Website Stats](https://docs.simpleanalytics.com/api/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | path | `string` | yes | Website hostname to query, for example `simpleanalytics.com`. |
| `start` | query | `string` | no | Start date or placeholder such as `today-30d`. |
| `end` | query | `string` | no | End date or placeholder such as `today`. |
| `fields` | query | `string` | no | Comma-separated stats fields such as `pageviews,visitors`. |
| `timezone` | query | `string` | no | IANA time zone such as `Europe/Amsterdam`. |
