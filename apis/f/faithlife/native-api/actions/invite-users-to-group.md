# Invite Users To Group with Faithlife

Creates invites for a group in Faithlife.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/invites`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [Invite Users To Group](https://developer.faithlife.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Faithlife group ID or token to invite users into. |
| `invites[0].accountId` | body | `string` | no | Optional Faithlife account ID to invite. |
| `invites[0].emailInvite.email` | body | `string` | no | Optional email address to invite when no account ID is provided. |
