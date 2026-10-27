# Microsoft Teams: Send Channel Message

Creates a new channel message in Microsoft Teams.

```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-channel-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-channel-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "channelId": "string",
  "body.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-channel-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "channelId": "string",
    "body.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | list | yes | Microsoft Graph team ID. |
| `channelId` | list | yes | Microsoft Graph channel ID. |
| `body.content` | string | yes | Message body content. |
| `body.contentType` | list<string> | no | Choose text or HTML. HTML must be supplied explicitly; Markdown is not converted. One of: `html`, `text`. Default: `text`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | Message body. Set Content Type to HTML when referencing attachments. |
| `attachments[]` | array<object> | no | Files already stored in SharePoint/OneDrive or supported cards. This does not upload file bytes. |
| `attachments[].id` | string | no | Match this ID in body.content using <attachment id="ID"></attachment> and choose HTML. |
| `attachments[].contentType` | string | no | Use reference for an existing file link, or a documented supported card media type. |
| `attachments[].contentUrl` | string | no | Existing file URL or share link accessible to recipients. Mutually exclusive with Content. |
| `attachments[].content` | string | no | Serialized card content. Mutually exclusive with Content URL. |
| `attachments[].name` | string | no | Attachment display name. |
| `attachments[].thumbnailUrl` | string | no | Optional thumbnail image URL. |
| `attachments[].teamsAppId` | string | no | Teams app associated with the attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "deletedDateTime": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "from": {},
      "id": "string",
      "importance": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "mentions": [
        {}
      ],
      "messageType": "string",
      "reactions": [
        {}
      ],
      "replyToId": "string",
      "subject": "string",
      "summary": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Message attachments. |
| `body` | object | Message body content. |
| `createdDateTime` | date | Timestamp at which the message was created. |
| `deletedDateTime` | date | Timestamp at which the message was deleted, when applicable. |
| `etag` | string | Version tag for the message. |
| `from` | object | Sender identity. |
| `id` | string | Unique identifier for the message. |
| `importance` | string | Importance of the message. |
| `lastModifiedDateTime` | date | Timestamp at which the message was last modified. |
| `locale` | string | Locale of the message. |
| `mentions` | array<object> | Mentions included in the message. |
| `messageType` | string | Type of chat message. |
| `reactions` | array<object> | Message reactions. |
| `replyToId` | string | ID of the parent message when this item is a reply. |
| `subject` | string | Subject of the message. |
| `summary` | string | Summary text for the message. |
| `webUrl` | string | Link to the message in Microsoft Teams. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/teams/:teamId/channels/:channelId/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-channel-message.md) for the provider-specific parameters and requirements.

