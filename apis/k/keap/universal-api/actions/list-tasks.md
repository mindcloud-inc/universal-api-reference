# Keap: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-tasks?${params}`, {
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
      "assignedToUserId": "string",
      "completed": true,
      "contactId": "string",
      "createdByUserId": "string",
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modificationTime": "2026-05-07T12:00:00.000Z",
      "priority": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string |  |
| `completed` | boolean |  |
| `contactId` | string |  |
| `createdByUserId` | string |  |
| `createTime` | date |  |
| `id` | string |  |
| `modificationTime` | date |  |
| `priority` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Keap API, this operation is `GET /tasks` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

