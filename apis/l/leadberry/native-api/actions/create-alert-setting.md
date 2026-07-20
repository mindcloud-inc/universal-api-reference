# Create Alert Setting with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/saveNewAlertSetting`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Create Alert Setting](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aid` | body | `string` | no | Leadberry account ID for the selected alert view. |
| `emails[]` | body | `string` | no | Email addresses that should receive the alert. |
| `freq` | body | `string` | no | Leadberry alert frequency such as default, everyday, everyweek, or realtime. |
| `pid` | body | `string` | no | Leadberry profile ID for the selected alert view. |
| `url` | body | `string` | no | Alert URL value used by Leadberry. The bundle sets this to an empty string for the standard flow. |
| `wid` | body | `string` | no | Leadberry website ID for the selected alert view. |
