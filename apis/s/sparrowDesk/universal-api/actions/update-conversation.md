# SparrowDesk: Update Conversation

Updates an existing conversation in SparrowDesk.

```
PUT https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no | Updated assignee email address. |
| `id` | number | yes | SparrowDesk conversation ID. |
| `priority` | string | no | Updated priority value. |
| `source` | string | no | Updated source value. |
| `status` | string | no | Updated status value. |
| `subject` | string | no | Updated conversation subject. |
| `teamId` | string | no | Updated team assignment. |

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

Through the native SparrowDesk API, this operation is `PATCH /conversations/{{id}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

