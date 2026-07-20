# Salesflare: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-tasks?${params}`, {
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
| `limit` | number | no | Maximum number of tasks to return. |
| `orderBy` | string | no | Sort expression such as due_date desc. |
| `search` | string | no | Free-text search across tasks. |
| `offset` | number | no | Number of tasks to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "assignees": [
        {}
      ],
      "completed": true,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "reminderDate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `assignees` | array<object> |  |
| `completed` | boolean |  |
| `creationDate` | date |  |
| `description` | string |  |
| `id` | number |  |
| `modificationDate` | date |  |
| `reminderDate` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET tasks` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

