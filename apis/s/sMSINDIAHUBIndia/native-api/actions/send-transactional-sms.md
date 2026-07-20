# Send Transactional SMS with SMSINDIAHUB (India)

## Endpoint

- **Method:** `GET`
- **Path:** `/vendorsms/pushsms.aspx`
- **Base URL:** `https://cloud.smsindiahub.in`
- **Official documentation:** [Send Transactional SMS](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | query | `string` | yes | Single recipient number or a comma-separated list of up to 100 numbers. |
| `sid` | query | `string` | yes | Approved sender ID. |
| `msg` | query | `string` | yes | SMS message text. |
