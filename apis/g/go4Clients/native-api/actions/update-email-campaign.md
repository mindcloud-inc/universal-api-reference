# Update Email Campaign with Go4Clients

Updates an existing email campaign in Go4Clients.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/campaigns/email/v1.0/{{campaignId}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Update Email Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Email campaign identifier. |
| `name` | body | `string` | yes | New name of the campaign. |
| `template` | body | `object` | no | New template body or template object used by the email. |
| `description` | body | `string` | no | Optional campaign description. |
| `numberOfEmail` | body | `number` | no | Sending rate quantity for the campaign. |
| `minutes` | body | `number` | no | Time frame in minutes for the sending rate. |
| `campaignStatus` | body | `string` | no | Campaign status value. |
| `subject` | body | `string` | yes | Subject of the email campaign. |
| `fromEmail` | body | `string` | yes | From email used on the campaign. |
| `replyEmail` | body | `string` | yes | Reply email for the campaign. |
