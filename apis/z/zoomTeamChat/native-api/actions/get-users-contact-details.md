# Get User's Contact Details with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/me/contacts/:identifier`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Get User's Contact Details](https://developers.zoom.us/docs/api/rest/reference/chat/methods/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The contact's user ID, email address, or member ID. |
| `query_presence_status` | query | `boolean` | no | Whether to include the contact's presence status. |
