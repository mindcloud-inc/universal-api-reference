# Update Alert Setting with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/updateAlertSetting`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Update Alert Setting](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aid` | body | `string` | no | Leadberry account ID for the alert view. |
| `alert_setting_id` | body | `string` | no | Leadberry alert setting identifier. |
| `alert_url_id` | body | `string` | no | Leadberry alert URL identifier. |
| `emails[]` | body | `string` | no | Email addresses for the alert. |
| `freq` | body | `string` | no | Leadberry alert frequency value. |
| `pid` | body | `string` | no | Leadberry profile ID for the alert view. |
| `type` | body | `string` | no | Leadberry alert email type, such as default or custom. |
| `url` | body | `string` | no | Alert URL value. |
| `wid` | body | `string` | no | Leadberry website ID for the alert view. |
