# LOBSTR.IO: Add Tasks

Creates new tasks in LOBSTR.IO.

```
POST https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/add-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/add-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "squid": "string",
  "tasks[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/add-tasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "squid": "string",
    "tasks[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `squid` | string | yes | The squid hash ID to add tasks to. |
| `tasks[]` | array<object> | yes | The array of task payloads to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duplicatedCount": 1,
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duplicatedCount` | number |  |
| `tasks` | array<object> |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `POST /v1/tasks` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tasks.md) for the provider-specific parameters and requirements.

