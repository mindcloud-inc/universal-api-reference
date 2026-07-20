# Morgen: Update Task

Updates a task in Morgen.

```
PUT https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morgen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Morgen task ID. |
| `title` | string | no | Updated title. |
| `description` | string | no | Updated description. |
| `due` | string | no | Updated due date in LocalDateTime format. Example: `2026-03-21T11:00:00`. |
| `timeZone` | string | no | Updated timezone. Example: `America/Argentina/Buenos_Aires`. |
| `priority` | number | no | Updated priority 0-9. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morgen API returns.

## Native endpoint

Through the native Morgen API, this operation is `POST /v3/tasks/update` (base URL `https://api.morgen.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

