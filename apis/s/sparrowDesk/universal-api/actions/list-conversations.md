# SparrowDesk: List Conversations

Retrieves conversations from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "pages": {
        "perPage": 1
      },
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
      ],
      "totalCount": 1
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
| `pages.perPage` | number | Page size. |
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
| `totalCount` | number | Total number of conversations. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /conversations` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

