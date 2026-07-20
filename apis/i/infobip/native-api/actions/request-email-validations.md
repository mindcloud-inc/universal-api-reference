# Request Email Validations with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/email/2/validations`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Request Email Validations](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `validationRequestId` | body | `string` | no | Unique identifier for the bulk email validation request. Provide your own or leave it blank to have one generated automatically. |
| `destinations` | body | `list<object>` | yes | Array of email addresses to be validated. |
| `destinations.destination` | body | `string` | no | The email address to be validated. |
