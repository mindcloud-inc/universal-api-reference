# Get Event Counts with Simple Analytics

Retrieves specified event counts from Simple Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{hostname}}.json`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Get Event Counts](https://docs.simpleanalytics.com/api/stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | path | `string` | yes | Website hostname to query, for example `simpleanalytics.com`. |
| `start` | query | `string` | no | Start date or placeholder such as `yesterday`. |
| `end` | query | `string` | no | End date or placeholder such as `today`. |
| `timezone` | query | `string` | no | IANA time zone such as `Europe/Amsterdam`. |
| `events` | query | `string` | yes | Comma-separated event names, or `*` for all events. |
