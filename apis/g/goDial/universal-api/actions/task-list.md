# GoDial: List Tasks

Retrieves a list of tasks from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-list?${params}`, {
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
      "accountsId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "desc": "string",
      "done": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountsId` | string |  |
| `createdOn` | date |  |
| `desc` | string |  |
| `done` | boolean |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/tasks/list` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/task-list.md) for the provider-specific parameters and requirements.

