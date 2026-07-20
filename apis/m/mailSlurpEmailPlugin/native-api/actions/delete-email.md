# Delete Email with MailSlurp Email Plugin

Deletes an existing email from MailSlurp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/emails/:emailId`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Delete Email](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/deleteEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | no | The MailSlurp email ID to delete. |
