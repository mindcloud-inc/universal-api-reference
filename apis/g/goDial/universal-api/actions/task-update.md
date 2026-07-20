# GoDial: Update Task

Updates an existing task in GoDial.

```
PUT https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Task ID. |
| `name` | string | yes | Provide new name of the Task |

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

Through the native GoDial API, this operation is `PUT /externals/tasks/[:id]/update` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/task-update.md) for the provider-specific parameters and requirements.

