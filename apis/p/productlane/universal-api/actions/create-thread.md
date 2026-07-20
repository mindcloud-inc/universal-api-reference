# Productlane: Create Thread

Creates a new thread in Productlane.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "painLevel": "string",
  "contactEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "painLevel": "string",
    "contactEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes |  |
| `painLevel` | string | yes |  |
| `contactEmail` | string | yes |  |
| `title` | string | no |  |
| `state` | string | no |  |
| `origin` | string | no |  |
| `contactName` | string | no |  |
| `assigneeId` | string | no |  |
| `projectId` | string | no |  |
| `issueId` | string | no |  |
| `companyId` | string | no |  |
| `createdAt` | date | no |  |
| `updatedAt` | date | no |  |
| `notify` | object | no |  |

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
      "company": {},
      "companyId": "string",
      "contact": {},
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
      "linkedIssues": [
        {}
      ],
      "linkedProjects": [
        {}
      ],
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
      "text": "string",
      "title": "string",
      "uniqueId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "videoId": "string",
      "workspace": {},
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
| `company` | object |  |
| `companyId` | string |  |
| `contact` | object |  |
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
| `linkedIssues` | array<object> |  |
| `linkedProjects` | array<object> |  |
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
| `text` | string |  |
| `title` | string |  |
| `uniqueId` | string |  |
| `updatedAt` | date |  |
| `videoId` | string |  |
| `workspace` | object |  |
| `workspaceId` | string |  |
| `zendeskId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `POST /threads` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thread.md) for the provider-specific parameters and requirements.

