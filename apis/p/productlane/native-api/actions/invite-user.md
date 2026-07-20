# Invite User with Productlane

Invites a user to your Productlane workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/invite`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Invite User](https://productlane.mintlify.dev/docs/api/users/invite-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to invite. |
| `name` | body | `string` | yes | Display name for the invited user. |
| `role` | body | `string` | yes | Initial role for the invited user. |
