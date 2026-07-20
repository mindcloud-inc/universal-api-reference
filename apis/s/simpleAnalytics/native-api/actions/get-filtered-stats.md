# Get Filtered Stats with Simple Analytics

Retrieves filtered stats from Simple Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{hostname}}.json`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Get Filtered Stats](https://docs.simpleanalytics.com/api/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | path | `string` | yes | Website hostname to query. |
| `start` | query | `string` | no | Start date like 2026-04-01, today, or today-30d. |
| `end` | query | `string` | no | End date like 2026-04-14, yesterday, or today. |
| `limit` | query | `string` | no | Limit returned breakdown rows between 1 and 1000. |
| `timezone` | query | `string` | no | Timezone like Europe/Amsterdam or UTC. |
| `info` | query | `string` | no | Include informational helper fields in the response. |
| `callback` | query | `string` | no | Wrap the response in a JSONP callback. |
| `events` | query | `string` | no | Comma-separated event names or * to return all events. |
| `interval` | query | `string` | no | Histogram interval: hour, day, week, month, or year. |
| `fields` | query | `string` | no | Comma-separated fields like histogram,pages,countries or seconds_on_page. |
| `page` | query | `string` | no | Filter by one page path. |
| `pages` | query | `string` | no | Filter by comma-separated page paths or wildcard patterns. |
| `country` | query | `string` | no | Filter by one country code. |
| `referrer` | query | `string` | no | Filter by one normalized referrer. |
| `utm_source` | query | `string` | no | Filter by one UTM source. |
| `utm_medium` | query | `string` | no | Filter by one UTM medium. |
| `utm_campaign` | query | `string` | no | Filter by one UTM campaign. |
| `utm_content` | query | `string` | no | Filter by one UTM content. |
| `utm_term` | query | `string` | no | Filter by one UTM term. |
| `browser_name` | query | `string` | no | Filter by one browser name. |
| `os_name` | query | `string` | no | Filter by one operating system name. |
| `device_type` | query | `string` | no | Filter by one device type. |
