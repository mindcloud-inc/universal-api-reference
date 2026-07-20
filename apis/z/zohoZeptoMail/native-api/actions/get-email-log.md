# Get Email Log with Zoho ZeptoMail

Retrieves a specific email log from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `email/email-reference/:emailReference`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Get Email Log](https://www.zoho.com/zeptomail/help/api/get-specific-email-log.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailReference` | path | `string` | yes | Unique email reference returned by ZeptoMail. |
