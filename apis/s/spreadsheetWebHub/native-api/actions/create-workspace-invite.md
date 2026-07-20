# Create Workspace Invite with SpreadsheetWeb Hub

Creates a new workspace invite in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites/create`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Create Workspace Invite](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.workspaceId` | body | `string` | no | SpreadsheetWeb workspace UUID. |
| `request.email` | body | `string` | no | Invitee email address. |
| `request.message` | body | `string` | no | Optional invite message. |
| `request.userTemplateId` | body | `string` | no | Template user UUID applied to the invite. |
| `request.externalLoginProvider` | body | `number` | no | External login provider enum value. |
