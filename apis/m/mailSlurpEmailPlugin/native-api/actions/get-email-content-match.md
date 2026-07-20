# Get Email Content Match with MailSlurp Email Plugin

Finds regex matches in a MailSlurp email body.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:emailId/contentMatch`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Get Email Content Match](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmailContentMatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | no | The MailSlurp email ID to search for pattern matches. |
