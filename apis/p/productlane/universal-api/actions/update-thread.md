# Productlane: Update Thread

Updates an existing thread in Productlane.

```
PUT https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `text` | string | no |  |
| `title` | string | no |  |
| `painLevel` | string | no |  |
| `assigneeId` | string | no |  |
| `projectId` | string | no |  |
| `notify` | object | no |  |
| `state` | string | no |  |
| `contactId` | string | no |  |
| `companyId` | string | no |  |
| `tagIds[]` | array<string> | no |  |
| `updatedAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "attachments": [
        {}
      ],
      "companyId": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "frontId": "string",
      "hubspotId": "string",
      "id": "string",
      "intercomId": "string",
      "isDeleted": true,
      "isRead": true,
      "lastInboundMessageAt": "2026-05-07T12:00:00.000Z",
      "lastOutboundMessageAt": "2026-05-07T12:00:00.000Z",
      "lastStateChangeAt": "2026-05-07T12:00:00.000Z",
      "linearAttachmentId": "string",
      "origin": "string",
      "painLevel": "string",
      "plainId": "string",
      "productboardId": "string",
      "recordingId": "string",
      "reporterId": "string",
      "slackChannelId": "string",
      "slackReplyId": "string",
      "snoozedUntil": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "tags": [
        {}
      ],
      "text": "string",
      "title": "string",
      "uniqueId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "videoId": "string",
      "workspaceId": "string",
      "zendeskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string |  |
| `attachments` | array<object> |  |
| `companyId` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `frontId` | string |  |
| `hubspotId` | string |  |
| `id` | string |  |
| `intercomId` | string |  |
| `isDeleted` | boolean |  |
| `isRead` | boolean |  |
| `lastInboundMessageAt` | date |  |
| `lastOutboundMessageAt` | date |  |
| `lastStateChangeAt` | date |  |
| `linearAttachmentId` | string |  |
| `origin` | string |  |
| `painLevel` | string |  |
| `plainId` | string |  |
| `productboardId` | string |  |
| `recordingId` | string |  |
| `reporterId` | string |  |
| `slackChannelId` | string |  |
| `slackReplyId` | string |  |
| `snoozedUntil` | date |  |
| `state` | string |  |
| `tags` | array<object> |  |
| `text` | string |  |
| `title` | string |  |
| `uniqueId` | string |  |
| `updatedAt` | date |  |
| `videoId` | string |  |
| `workspaceId` | string |  |
| `zendeskId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `PATCH /threads/:id` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-thread.md) for the provider-specific parameters and requirements.

