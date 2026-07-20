# Get Template with Zoho ZeptoMail

Retrieves an email template from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `agents/:agentAlias/templates/:templateKey`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Get Template](https://www.zoho.com/zeptomail/help/api/get-template.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | path | `string` | yes | Template key to fetch. |
