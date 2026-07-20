# Toodledo: Share Task

Shares a task with a collaborator in Toodledo.

```
PUT https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/share-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/share-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "share": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/share-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "share": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Numeric Toodledo task ID to share. |
| `share` | string | yes | JSON-encoded array of collaborator user IDs that should share the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shared": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shared` | number | Task ID that was shared. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /tasks/share.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-task.md) for the provider-specific parameters and requirements.

