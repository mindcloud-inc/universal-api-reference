# Send Service SMS with TextingHouse

Creates a service SMS in TextingHouse.

## Endpoint

- **Method:** `POST`
- **Path:** `/do`
- **Base URL:** `https://api.textinghouse.com/http/v1`
- **Official documentation:** [Send Service SMS](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-envoimess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number in international format, including country code. |
| `txt` | body | `string` | yes | SMS content to send. |
| `climsgid` | body | `string` | no | Optional client-defined message identifier, up to 32 characters. Maximum length: 32. |
| `from` | body | `string` | no | Optional sender ID approved on your TextingHouse account. Maximum length: 11. |
