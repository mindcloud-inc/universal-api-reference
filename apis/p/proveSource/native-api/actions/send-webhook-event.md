# Send Webhook Event with ProveSource

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/track/:webhookId`
- **Base URL:** `https://api.provesrc.com`
- **Official documentation:** [Send Webhook Event](https://help.provesrc.com/en/articles/3474258-setup-a-custom-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The ProveSource notification webhook identifier to send this event to. |
| `email` | body | `string` | no | Email for the conversion or lead. Required for Stream notifications. |
| `firstName` | body | `string` | no | Lead first name shown in the notification when available. |
| `lastName` | body | `string` | no | Lead last name shown in the notification when available. |
| `timestamp` | body | `number` | no | Event timestamp in milliseconds or seconds. |
| `ip` | body | `string` | no | Visitor IP address used for location lookup. |
| `guid` | body | `string` | no | Optional product or category identifier used by ProveSource webhook notifications. |
| `city` | body | `string` | no | Optional city value for location enrichment. |
| `state` | body | `string` | no | Optional state name for US locations. |
| `stateCode` | body | `string` | no | Optional state code for US locations. |
| `country` | body | `string` | no | Optional country value for location enrichment. |
| `countryCode` | body | `string` | no | Optional two-letter country code for location enrichment. |
| `productName` | body | `string` | no | Optional product name appended to the notification text. |
| `productLink` | body | `string` | no | Optional product page URL used for click-through behavior. |
| `productImage` | body | `string` | no | Optional product image URL shown in the notification. |
| `total` | body | `number` | no | Optional purchase total amount. |
| `currency` | body | `string` | no | Optional purchase currency code. |
| `products[]` | body | `array<object>` | no | Optional array of product line items for multi-product purchases. Each item should include at least a name and link. |
