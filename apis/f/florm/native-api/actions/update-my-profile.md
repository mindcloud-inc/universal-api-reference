# Update My Profile with Florm

Updates your user profile in Florm.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/auth/me`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Update My Profile](https://api.florm.io/docs#/default/save_user_v1_auth_me_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the Florm profile. |
| `name` | body | `string` | yes | Display name for the Florm profile. |
| `settings.notifications_news` | body | `boolean` | yes | Whether to receive Florm news notifications. |
| `settings.notifications_events` | body | `boolean` | yes | Whether to receive Florm event notifications. |
| `settings.language` | body | `string` | yes | Language code for the Florm profile. |
