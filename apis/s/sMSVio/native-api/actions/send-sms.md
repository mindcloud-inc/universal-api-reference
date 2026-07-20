# Send SMS with SMSVio

## Endpoint

- **Method:** `POST`
- **Path:** `/services/send/`
- **Base URL:** `https://gate.smsvio.cz`
- **Official documentation:** [Send SMS](https://www.smsvio.cz/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | SMS body text to send |
| `number` | body | `string` | yes | Recipient phone number in international format |
| `devices` | body | `string` | no | — |
