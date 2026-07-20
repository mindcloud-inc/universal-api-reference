# Add Email to Campaign with Go4Clients

Adds email recipients to an existing Go4Clients campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/email/v1.0/{{campaignId}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Add Email to Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Email campaign identifier. |
| `destinationsList[]` | body | `array<string>` | yes | Email destination list. |
| `landingCustomFields` | body | `object` | yes | Map of custom fields keyed by destination email. |
| `fromEmail` | body | `string` | yes | From email used in the email sent. |
| `fromName` | body | `string` | no | From name associated to the sender email. |
| `subject` | body | `string` | no | Subject of the email. |
| `priority` | body | `string` | no | Priority of the email. |
