# Create Campaign with Emailchef

Creates a new campaign in Emailchef.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Create Campaign](https://emailchef.com/integration/#/Campaigns/createCampaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `instance_in.name` | body | `string` | yes |
| `instance_in.subject` | body | `string` | yes |
| `instance_in.sender_id` | body | `string` | yes |
| `instance_in.html_body` | body | `string` | no |
| `instance_in.lists[].list_id` | body | `string` | no |
