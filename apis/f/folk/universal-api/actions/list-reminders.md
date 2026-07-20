# folk: List Reminders

Retrieves a list of reminders from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-reminders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-reminders?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | no | Filter reminders by entity. Only reminders linked to the specified entity will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUsers": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "entity": {},
      "id": "string",
      "lastTriggerTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextTriggerTime": "2026-05-07T12:00:00.000Z",
      "recurrenceRule": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUsers` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `entity` | object |  |
| `id` | string |  |
| `lastTriggerTime` | date |  |
| `name` | string |  |
| `nextTriggerTime` | date |  |
| `recurrenceRule` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native folk API, this operation is `GET /v1/reminders` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

