# Create Email Campaign with Constant Contact

Creates an email campaign in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create Email Campaign](https://developer.constantcontact.com/api_guide/email_campaign_create.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique name for the email campaign. |
| `email_campaign_activities[]` | body | `array<object>` | yes | Array containing the email campaign activity content object. |
