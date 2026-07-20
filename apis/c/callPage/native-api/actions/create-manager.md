# Create Manager with CallPage

Creates a new manager in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/managers/create`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Create Manager](https://callpage.github.io/documentation-rest/#create-manager)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `number` | yes |
| `widget_id` | body | `number` | yes |
| `enabled` | body | `boolean` | yes |
| `business_times` | body | `list<object>` | no |
