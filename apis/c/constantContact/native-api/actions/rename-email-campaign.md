# Rename Email Campaign with Constant Contact

Renames an email campaign in Constant Contact.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/emails/:campaign_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Rename Email Campaign](https://developer.constantcontact.com/api_guide/email_campaigns_rename.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique identifier for an email campaign. |
| `name` | body | `string` | yes | Updated unique name for the email campaign. |
