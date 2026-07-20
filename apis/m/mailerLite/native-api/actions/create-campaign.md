# Create Campaign with MailerLite

Creates a new campaign in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Create Campaign](https://developers.mailerlite.com/docs/campaigns#create-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Campaign name. |
| `type` | body | `string` | yes | Campaign type. |
| `language_id` | body | `number` | no | Campaign language ID for unsubscribe content. |
| `emails[]` | body | `array<object>` | yes | Email variants for the campaign. |
| `emails[].subject` | body | `string` | yes | Email subject line. |
| `emails[].from_name` | body | `string` | yes | Verified sender name. |
| `emails[].from` | body | `string` | yes | Verified sender email address. |
| `emails[].reply_to` | body | `string` | no | Verified reply-to email address. |
| `emails[].content` | body | `string` | no | Optional HTML content for advanced-plan custom HTML campaigns. |
| `groups[]` | body | `array<string>` | no | Recipient group IDs. |
| `segments[]` | body | `array<string>` | no | Recipient segment IDs. Overrides groups when both are provided. |
| `settings` | body | `object` | no | Campaign settings object. |
| `settings.ecommerce_tracking` | body | `boolean` | no | Enable ecommerce link tracking for shop URLs. |
