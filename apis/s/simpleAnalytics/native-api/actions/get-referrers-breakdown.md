# Get Referrers Breakdown with Simple Analytics

Retrieves a referrer breakdown from Simple Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{hostname}}.json`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Get Referrers Breakdown](https://docs.simpleanalytics.com/api/stats)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `hostname` | path | `string` | yes |
| `start` | query | `string` | no |
| `end` | query | `string` | no |
| `timezone` | query | `string` | no |
