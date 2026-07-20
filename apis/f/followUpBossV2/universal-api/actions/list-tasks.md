# Follow Up Boss: List Tasks

Retrieves tasks from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-tasks?${params}`, {
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
      "metadata": {
        "collection": "string",
        "limit": 1,
        "next": {},
        "nextLink": {},
        "offset": 1,
        "total": 1
      },
      "tasks": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `metadata.collection` | string |  |
| `metadata.limit` | number |  |
| `metadata.next` | object |  |
| `metadata.nextLink` | object |  |
| `metadata.offset` | number |  |
| `metadata.total` | number |  |
| `tasks[]` | array<object> |  |
| `tasks[].assignedTo` | string |  |
| `tasks[].assignedUserId` | number |  |
| `tasks[].completed` | object |  |
| `tasks[].created` | string |  |
| `tasks[].createdBy` | string |  |
| `tasks[].createdById` | number |  |
| `tasks[].dueDate` | object |  |
| `tasks[].dueDateTime` | object |  |
| `tasks[].externalCalendarId` | object |  |
| `tasks[].externalTaskLink` | object |  |
| `tasks[].id` | number |  |
| `tasks[].isCompleted` | number |  |
| `tasks[].name` | string |  |
| `tasks[].personId` | number |  |
| `tasks[].remindSecondsBefore` | object |  |
| `tasks[].type` | string |  |
| `tasks[].updated` | string |  |
| `tasks[].updatedBy` | string |  |
| `tasks[].updatedById` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET tasks` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

