# Create Email Campaign with Sarbacane

Creates a new email campaign in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/email`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Create Email Campaign](https://developers.sarbacane.com/campaigns/#create-an-email-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aliasFrom` | body | `string` | no | Sender display name. |
| `aliasReplyTo` | body | `string` | no | Reply-to display name. |
| `emailFrom` | body | `string` | no | Sender email address. |
| `emailReplyTo` | body | `string` | no | Reply-to email address. |
| `name` | body | `string` | no | Campaign name. |
| `preheader` | body | `string` | no | Campaign preheader text. |
| `subject` | body | `string` | no | Campaign subject. |
