# Front: List Assigned Conversations

Retrieves conversations assigned to a teammate in Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-assigned-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-assigned-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0&teammateId=tea_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teammateId": "tea_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-assigned-conversations?${params}`, {
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
| `teammateId` | string | yes | The teammate ID. Example: `tea_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Search query object string for statuses or ticketing status filters. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "createdAt": 1,
      "customFields": {},
      "id": "string",
      "isPrivate": true,
      "links": [
        {}
      ],
      "metadata": {},
      "recipient": {},
      "scheduledReminders": [
        {}
      ],
      "status": "string",
      "statusCategory": "string",
      "statusId": "string",
      "subject": "string",
      "tags": [
        {}
      ],
      "ticketIds": [
        "string"
      ],
      "updatedAt": 1,
      "waitingSince": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `createdAt` | number |  |
| `customFields` | object |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `links` | array<object> |  |
| `metadata` | object |  |
| `recipient` | object |  |
| `scheduledReminders` | array<object> |  |
| `status` | string |  |
| `statusCategory` | string |  |
| `statusId` | string |  |
| `subject` | string |  |
| `tags` | array<object> |  |
| `ticketIds` | array<string> |  |
| `updatedAt` | number |  |
| `waitingSince` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /teammates/:teammate_id/conversations` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assigned-conversations.md) for the provider-specific parameters and requirements.

