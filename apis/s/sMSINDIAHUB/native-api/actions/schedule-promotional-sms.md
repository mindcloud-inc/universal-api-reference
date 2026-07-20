# Schedule Promotional SMS with SMSINDIAHUB

Schedules a promotional SMS message in SMSINDIAHUB.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendorsms/pushsms.aspx`
- **Base URL:** `https://cloud.smsindiahub.in`
- **Official documentation:** [Schedule Promotional SMS](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | query | `string` | yes | One or more destination mobile numbers, separated by commas. |
| `sid` | query | `string` | yes | The approved sender ID. |
| `msg` | query | `string` | yes | The SMS message content. |
| `schedtime` | query | `string` | yes | The scheduled send time in `yyyy/mm/dd hh:mm:ss PM` format. |
