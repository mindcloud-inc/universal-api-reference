# Create Invite with Discourse

Creates a new invite in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Invite](https://docs.discourse.org/#tag/Invites/operation/createInvite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Invitee email address. |
| `skip_email` | body | `boolean` | no | Create the invite without sending the email. |
