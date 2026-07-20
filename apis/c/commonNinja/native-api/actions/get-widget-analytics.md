# Get Widget Analytics with Common Ninja

Retrieves widget analytics from Common Ninja.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets/:id/analytics`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [Get Widget Analytics](https://developers.commoninja.com/docs/api/analytics/widget-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdown` | query | `string` | no | Analytics breakdown value. |
| `endDate` | query | `string` | no | End date for the analytics period. |
| `events` | query | `string` | no | Comma-separated analytics events to include. |
| `id` | path | `string` | yes | The widget ID. |
| `startDate` | query | `string` | no | Start date for the analytics period. |
