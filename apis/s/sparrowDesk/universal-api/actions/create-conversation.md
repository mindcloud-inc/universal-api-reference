# SparrowDesk: Create Conversation

Creates a conversation in SparrowDesk.

```
POST https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "requestedBy": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "requestedBy": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no | Assignee email address. |
| `brandId` | number | no | Optional SparrowDesk brand ID. |
| `description` | string | yes | Conversation description text. |
| `priority` | string | no | Priority: Low, Medium, High, or Urgent. |
| `requestedBy` | string | yes | Requester email address or phone number. |
| `source` | string | no | Source: Mail or Call. |
| `status` | string | no | Status: Open, Pending, Resolved, or Closed. |
| `subject` | string | yes | Conversation subject. |
| `teamId` | number | no | Optional SparrowDesk team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToMemberId": 1,
      "assignedToTeamId": 1,
      "brand": "string",
      "brandId": 1,
      "createdAt": 1,
      "customFields": [
        {}
      ],
      "descriptionHtml": "string",
      "descriptionText": "string",
      "due": 1,
      "firstResponseDue": 1,
      "firstResponseTime": 1,
      "id": 1,
      "lastUpdatedAt": 1,
      "priority": "string",
      "properties": {},
      "requestedByEmail": "ava@example.com",
      "requestedById": 1,
      "requestedByPhone": "string",
      "resolutionTime": 1,
      "source": "string",
      "status": "string",
      "subject": "string",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToMemberId` | number | Assigned member ID. |
| `assignedToTeamId` | number | Assigned team ID. |
| `brand` | string | Brand name. |
| `brandId` | number | Brand ID. |
| `createdAt` | number | Creation timestamp. |
| `customFields` | array<object> | Conversation custom field values. |
| `descriptionHtml` | string | HTML description. |
| `descriptionText` | string | Plain-text description. |
| `due` | number | Due timestamp when present. |
| `firstResponseDue` | number | First response due timestamp when present. |
| `firstResponseTime` | number | First response timestamp when present. |
| `id` | number | Conversation ID. |
| `lastUpdatedAt` | number | Last update timestamp. |
| `priority` | string | Conversation priority. |
| `properties` | object | Conversation metadata properties. |
| `requestedByEmail` | string | Requester email address. |
| `requestedById` | number | Requester contact ID. |
| `requestedByPhone` | string | Requester phone number. |
| `resolutionTime` | number | Resolution timestamp when present. |
| `source` | string | Conversation source. |
| `status` | string | Conversation status. |
| `subject` | string | Conversation subject. |
| `tags` | array<object> | Conversation tags. |

## Native endpoint

Through the native SparrowDesk API, this operation is `POST /conversations` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

