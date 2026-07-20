# Productlane: Get Thread

Retrieves a thread from your Productlane workspace.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-thread?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-thread?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "assigneeId": "string",
      "attachments": [
        {}
      ],
      "company": {},
      "companyId": "string",
      "contact": {},
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerNeeds": [
        {}
      ],
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
      "reporter": {},
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
| `assignee` | object |  |
| `assigneeId` | string |  |
| `attachments` | array<object> |  |
| `company` | object |  |
| `companyId` | string |  |
| `contact` | object |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `customerNeeds` | array<object> |  |
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
| `reporter` | object |  |
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

Through the native Productlane API, this operation is `GET /threads/:id` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.

