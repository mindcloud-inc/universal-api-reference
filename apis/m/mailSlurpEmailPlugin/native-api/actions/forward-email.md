# Forward Email with MailSlurp Email Plugin

Forwards an existing email from MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:emailId/forward`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Forward Email](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/forwardEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | no | The MailSlurp email ID to forward. |
