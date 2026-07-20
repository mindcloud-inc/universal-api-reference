# Mark Email Read State with MailSlurp Email Plugin

Updates an email's read state in MailSlurp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/emails/:emailId/read`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Mark Email Read State](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/markAsRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | no | The MailSlurp email ID to update. |
