# Microsoft 365 Planner: Create Bucket



```
POST https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Backlog",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Backlog",
    "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new Planner bucket. Example: `Backlog`. |
| `planId` | string | yes | Planner plan ID where the bucket should be created. Example: `xqQg5FS2LkCp935s-FIFm2QAFkHM`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "orderHint": "string",
      "planId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `orderHint` | string |  |
| `planId` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `POST /v1.0/planner/buckets` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bucket.md) for the provider-specific parameters and requirements.

