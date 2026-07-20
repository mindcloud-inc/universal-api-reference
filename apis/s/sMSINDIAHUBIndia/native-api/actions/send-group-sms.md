# Send Group SMS with SMSINDIAHUB (India)

## Endpoint

- **Method:** `GET`
- **Path:** `/vendorsms/pushsms.aspx`
- **Base URL:** `https://cloud.smsindiahub.in`
- **Official documentation:** [Send Group SMS](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | query | `string` | yes | Comma-separated list of recipient mobile numbers. |
| `sid` | query | `string` | yes | Approved sender ID. |
| `msg` | query | `string` | yes | SMS message text. |
