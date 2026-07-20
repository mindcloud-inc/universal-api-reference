# Verify Message Code with TopMessage

Verifies a message code by recipient number in TopMessage.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Verify Message Code](https://topmessage.com/documentation-api/get-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | query | `string` | yes | The recipient phone number in international format. |
| `code` | query | `string` | yes | The verification code to validate. |
| `expired` | query | `boolean` | no | When true, include expired verification codes in the lookup. |
