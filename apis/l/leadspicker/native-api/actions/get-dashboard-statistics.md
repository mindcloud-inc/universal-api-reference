# Get Dashboard Statistics with Leadspicker

Retrieves dashboard statistics from Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/dashboard/stats`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [Get Dashboard Statistics](https://app.leadspicker.com/app/sb/api/docs#/Dashboard/apps_salesbooster_api_get_dashboard_stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_frame` | query | `string` | no | Dashboard time frame filter. |
| `custom_start_date` | query | `date` | no | Dashboard custom start date. |
| `custom_end_date` | query | `date` | no | Dashboard custom end date. |
