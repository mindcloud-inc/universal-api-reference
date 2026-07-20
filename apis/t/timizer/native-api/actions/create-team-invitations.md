# Create Team Invitations with Timizer

Creates team invitations and users if needed in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/admin-teams/:teamId/invitations`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Team Invitations](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | ID of the team. |
| `invitations[]` | body | `array<object>` | no | Invitation entries to create. |
| `invitations[].email` | body | `string` | no | Email address for the invited user. |
| `invitations[].firstName` | body | `string` | no | Optional first name. |
| `invitations[].lastName` | body | `string` | no | Optional last name. |
| `invitations[].note` | body | `string` | no | Invitation note. |
| `invitations[].isExternalUser` | body | `boolean` | no | Whether the invited member is external to your main company. |
| `sendEmails` | body | `boolean` | no | Whether invitation emails should be sent. |
