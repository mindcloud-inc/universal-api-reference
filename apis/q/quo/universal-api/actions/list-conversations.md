# Quo: List Conversations

Retrieves all existing conversations from Quo.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-conversations?${params}`, {
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
| `createdAfter` | date | no |  |
| `createdBefore` | date | no |  |
| `excludeInactive` | boolean | no |  |
| `phoneNumbers[]` | array<string> | no |  |
| `updatedAfter` | date | no |  |
| `updatedBefore` | date | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastActivityAt": "2026-05-07T12:00:00.000Z",
      "lastActivityId": "string",
      "mutedUntil": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "participants": [
        "string"
      ],
      "phoneNumberId": "string",
      "snoozedUntil": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `id` | string |  |
| `lastActivityAt` | date |  |
| `lastActivityId` | string |  |
| `mutedUntil` | date |  |
| `name` | string |  |
| `participants` | array<string> |  |
| `phoneNumberId` | string |  |
| `snoozedUntil` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Quo API, this operation is `GET /conversations` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

