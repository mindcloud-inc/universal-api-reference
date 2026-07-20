# Update Campaign with MailerLite

Updates a draft campaign in MailerLite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaignId`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Update Campaign](https://developers.mailerlite.com/docs/campaigns#update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Draft campaign ID to update. |
| `name` | body | `string` | yes | Campaign name. |
| `language_id` | body | `number` | no | Campaign language ID for unsubscribe content. |
| `emails[]` | body | `array<object>` | yes | Email variants for the campaign. |
| `emails[].subject` | body | `string` | yes | Email subject line. |
| `emails[].from_name` | body | `string` | yes | Verified sender name. |
| `emails[].from` | body | `string` | yes | Verified sender email address. |
| `emails[].content` | body | `string` | no | Optional HTML content for advanced-plan custom HTML campaigns. |
| `groups[]` | body | `array<string>` | no | Recipient group IDs. |
| `segments[]` | body | `array<string>` | no | Recipient segment IDs. Overrides groups when both are provided. |
