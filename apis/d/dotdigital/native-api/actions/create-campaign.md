# Create Campaign with Dotdigital

Creates a new campaign in Dotdigital.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/campaigns`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Create Campaign](https://developer.dotdigital.com/reference/create-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the campaign being created |
| `subject` | body | `string` | yes | The email subject line of the campaign |
| `fromName` | body | `string` | yes | The from name of the campaign |
| `htmlContent` | body | `string` | yes | The HTML content of the campaign |
| `plainTextContent` | body | `string` | yes | The plain text content of the campaign |
| `fromAddress.email` | body | `string` | no | — |
| `fromAddress.id` | body | `number` | no | — |
| `replyAction` | body | `string` | no | — |
| `replyToAddress` | body | `string` | no | — |
| `type` | body | `list<string>` | no | Accepted values: `Standard`, `Triggered`. |
