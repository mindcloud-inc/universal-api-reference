# Get Ad Account Stats with Snapchat Ads

Retrieves ad account performance stats from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/adaccounts/:adAccountId/stats`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Get Ad Account Stats](https://developers.snap.com/api/marketing-api/Ads-API/measurement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID to report on. |
| `granularity` | query | `string` | yes | The reporting granularity, such as TOTAL, DAY, or HOUR. |
| `start_time` | query | `date` | no | The report start time in Snapchat's expected timestamp format. |
| `end_time` | query | `date` | no | The report end time in Snapchat's expected timestamp format. |
| `fields` | query | `string` | yes | Comma-separated Snapchat stats fields to return. |
| `breakdown` | query | `string` | no | Optional Snapchat stats breakdown. |
