# Get Email Codes with MailSlurp Email Plugin

Extracts verification codes from an email in MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:emailId/codes`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Get Email Codes](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmailCodes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | no | The MailSlurp email ID to inspect for verification codes. |
