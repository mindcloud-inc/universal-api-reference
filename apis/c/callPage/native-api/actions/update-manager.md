# Update Manager with CallPage

Updates an existing manager in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/managers/update`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update Manager](https://callpage.github.io/documentation-rest/#update-manager)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `number` | yes |
| `widget_id` | body | `number` | yes |
| `enabled` | body | `boolean` | yes |
| `business_times` | body | `list<object>` | no |
