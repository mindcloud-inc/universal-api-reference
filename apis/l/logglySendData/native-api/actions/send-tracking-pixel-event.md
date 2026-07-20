# Send Tracking Pixel Event with Loggly (Send Data)

Creates a tracking-pixel log event in Loggly.

## Endpoint

- **Method:** `GET`
- **Path:** `/inputs/:customerToken.gif`
- **Base URL:** `https://logs-01.loggly.com`
- **Official documentation:** [Send Tracking Pixel Event](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/tracking-pixel.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerToken` | path | `string` | yes |
| `message` | query | `string` | yes |
