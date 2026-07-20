# Cirra: Create Thread

Creates a Cirra thread and starts its initial run.

```
POST https://connect.mindcloud.co/v1/universal/cirra/latest/actions/create-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/create-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/create-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The first user message to add to the new thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "runId": "string",
      "status": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `runId` | string | The initial run ID. |
| `status` | string | The accepted run-start status. |
| `threadId` | string | The created thread ID. |

## Native endpoint

Through the native Cirra API, this operation is `POST /v1/cirra/threads` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thread.md) for the provider-specific parameters and requirements.

