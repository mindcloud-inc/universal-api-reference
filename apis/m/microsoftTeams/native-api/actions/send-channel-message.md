# Send Channel Message with Microsoft Teams

Creates a new channel message in Microsoft Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Send Channel Message](https://learn.microsoft.com/en-us/graph/api/channel-post-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `list` | yes | Microsoft Graph team ID. |
| `channelId` | path | `list` | yes | Microsoft Graph channel ID. |
| `body.content` | body | `string` | yes | Message body content. |
| `body.contentType` | body | `list<string>` | no | Choose text or HTML. HTML must be supplied explicitly; Markdown is not converted. Accepted values: `html`, `text`. |
| `body` | body | `object` | no | Message body. Set Content Type to HTML when referencing attachments. |
| `attachments[]` | body | `array<object>` | no | Files already stored in SharePoint/OneDrive or supported cards. This does not upload file bytes. |
| `attachments[].id` | body | `string` | no | Match this ID in body.content using <attachment id="ID"></attachment> and choose HTML. |
| `attachments[].contentType` | body | `string` | no | Use reference for an existing file link, or a documented supported card media type. |
| `attachments[].contentUrl` | body | `string` | no | Existing file URL or share link accessible to recipients. Mutually exclusive with Content. |
| `attachments[].content` | body | `string` | no | Serialized card content. Mutually exclusive with Content URL. |
| `attachments[].name` | body | `string` | no | Attachment display name. |
| `attachments[].thumbnailUrl` | body | `string` | no | Optional thumbnail image URL. |
| `attachments[].teamsAppId` | body | `string` | no | Teams app associated with the attachment. |
