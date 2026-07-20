# Validate Sender for Voice with Seven

Creates a voice sender validation in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate_for_voice`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Validate Sender for Voice](https://docs.seven.io/en/rest-api/endpoints/sender-identifiers#validate-sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | The phone number to be validated. The format is almost arbitrary - our gateway automatically formats the number correctly. |
| `callback` | body | `string` | no | Callback URL to be called as soon as the validation has been successfully completed. |
