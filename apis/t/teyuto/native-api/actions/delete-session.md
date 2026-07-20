# Delete Session with Teyuto

Deletes an existing authenticated Teyuto session.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sessions`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Delete Session](https://docs.teyuto.com/api/delete-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | User ID whose session should be revoked. |
