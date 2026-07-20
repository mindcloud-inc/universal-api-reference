# Invite Users with Alpha TransForm

Invites users to create Alpha TransForm accounts.

## Endpoint

- **Method:** `POST`
- **Path:** `/inviteUsers/{accountId}`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Invite Users](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/InviteUsers.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | — |
| `usersToInvite` | body | `string` | no | email addresses of people to invite |
