# Bigjpg: Retry Task

Retries image enlargement tasks in Bigjpg by task ID.

```
PUT https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/retry-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigjpg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/retry-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskIds": "tid1,tid2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/retry-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskIds": "tid1,tid2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskIds` | string | yes | One or more Bigjpg task IDs to retry, comma-separated in the request path. Accepts multiple values in one string, delimited by `,`. Example: `tid1,tid2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Retry task status from Bigjpg. |
| `url` | string | Result image URL when available after retry. |

## Native endpoint

Through the native Bigjpg API, this operation is `POST /task/:taskIds` (base URL `https://bigjpg.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-task.md) for the provider-specific parameters and requirements.

