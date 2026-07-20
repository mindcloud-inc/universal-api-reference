# Get Callback Widget Statistics with Novofon

Retrieves callback widget statistics from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/statistics/callback_widget/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get Callback Widget Statistics](https://novofon.com/instructions/api/#statistics_callback_widget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | query | `string` | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `skip` | query | `string` | no | Optional number of rows to skip for pagination. |
| `start` | query | `string` | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
| `widget_id` | query | `string` | no | Optional callback widget identifier filter. |
