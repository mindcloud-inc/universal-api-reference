# Griptape: Create Thread

Creates a new thread in Griptape.

```
POST https://connect.mindcloud.co/v1/universal/griptape/latest/actions/create-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/create-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/create-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | no | Optional unique alias for the thread. |
| `name` | string | no | Optional thread name to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created_at": "string",
      "created_by": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organization_id": "string",
      "thread_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organization_id` | string |  |
| `thread_id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/threads` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thread.md) for the provider-specific parameters and requirements.

