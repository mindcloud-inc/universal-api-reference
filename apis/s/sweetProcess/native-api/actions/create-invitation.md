# Create Invitation with SweetProcess

Creates a new invitation in SweetProcess.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations/`
- **Base URL:** `https://www.sweetprocess.com/api/v1`
- **Official documentation:** [Create Invitation](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitations[]` | body | `array<object>` | no | One or more invitation objects to send to SweetProcess. |
| `invitations[].send_mail` | body | `boolean` | no | Whether SweetProcess should send an email for this invitation row. |
| `invitations[].content_type` | body | `string` | yes | The target object type for the invitation, for example team. |
| `invitations[].permission` | body | `string` | yes | The permission level to assign, for example view. |
| `invitations[].object_id` | body | `number` | yes | The numeric ID of the referenced team or document. |
| `invitations[].to_user_id` | body | `string` | yes | The SweetProcess user API URL that should receive the invitation. |
