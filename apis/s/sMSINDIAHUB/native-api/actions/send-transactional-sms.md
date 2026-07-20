# Send Transactional SMS with SMSINDIAHUB

Sends a transactional SMS message in SMSINDIAHUB.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendorsms/pushsms.aspx`
- **Base URL:** `https://cloud.smsindiahub.in`
- **Official documentation:** [Send Transactional SMS](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | query | `string` | yes | One or more destination mobile numbers, separated by commas. |
| `sid` | query | `string` | yes | The approved sender ID. |
| `msg` | query | `string` | yes | The SMS message content. |
