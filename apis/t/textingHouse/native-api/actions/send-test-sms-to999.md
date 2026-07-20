# Send Test SMS To 999 with TextingHouse

Creates a test SMS to 999 in TextingHouse.

## Endpoint

- **Method:** `POST`
- **Path:** `/do`
- **Base URL:** `https://api.textinghouse.com/http/v1`
- **Official documentation:** [Send Test SMS To 999](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-smstest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txt` | body | `string` | yes | SMS content to send to the TextingHouse test number. |
| `climsgid` | body | `string` | no | Optional client-defined message identifier, up to 32 characters. Maximum length: 32. |
