# Send Verification Message with Routee

Sends a verification message with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/telegram`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send Verification Message](https://docs.routee.net/reference/send-verification-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | body | `string` | yes | The phone number in E.164 format (e.g., `+306974444444`). |
| `requestId` | body | `string` | no | Unique identifier from the checkSendAbility method |
| `senderUsername` | body | `string` | no | Username of the Telegram channel |
| `code` | body | `string` | no | Custom verification code (4-8 numeric characters |
| `codeLength` | body | `string` | no | Length of the generated verification code (4-8) |
| `callbackUrl` | body | `string` | no | HTTPS URL to receive delivery reports |
| `payload` | body | `string` | no | Custom payload (0-128 bytes |
| `ttl` | body | `number` | no | Time-to-live in seconds (60-86400) |
