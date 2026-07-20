# Add Users To Widget with CallPage

Adds users to an existing widget in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/add-users`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Add Users To Widget](https://callpage.github.io/documentation-rest/#add-users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `user_id` | body | `list<number>` | yes |
| `business_times` | body | `list<object>` | no |
