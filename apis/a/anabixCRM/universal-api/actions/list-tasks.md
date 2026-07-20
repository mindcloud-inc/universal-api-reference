# Anabix CRM: List Tasks

Retrieves task records from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-tasks?${params}`, {
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
      "assignedUserId": 1,
      "assignedUsername": "Ava Chen",
      "body": "string",
      "category": "string",
      "completedDate": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "deadline": "2026-05-07T12:00:00.000Z",
      "deadlineTime": "string",
      "duration": "string",
      "idContact": 1,
      "idDeal": 1,
      "idTask": 1,
      "priority": "string",
      "revisionInfo": {},
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUserId` | number |  |
| `assignedUsername` | string |  |
| `body` | string |  |
| `category` | string |  |
| `completedDate` | date |  |
| `customFields` | array<object> |  |
| `deadline` | date |  |
| `deadlineTime` | string |  |
| `duration` | string |  |
| `idContact` | number |  |
| `idDeal` | number |  |
| `idTask` | number | Anabix task ID. |
| `priority` | string |  |
| `revisionInfo` | object |  |
| `status` | string |  |
| `title` | string | Task title. |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

