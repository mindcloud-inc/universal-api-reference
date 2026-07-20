# Send Phone Code with Didit

Sends a phone verification code in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/phone/send/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Send Phone Code](https://docs.didit.me/standalone-apis/phone-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | body | `string` | yes | Phone number to verify. |
