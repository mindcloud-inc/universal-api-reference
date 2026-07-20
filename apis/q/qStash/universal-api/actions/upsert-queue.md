# QStash: Upsert Queue

Creates a QStash queue, or updates one if it exists.

```
POST https://connect.mindcloud.co/v1/universal/qStash/latest/actions/upsert-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/upsert-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "queueName": "Ava Chen",
  "parallelism": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/upsert-queue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "queueName": "Ava Chen",
    "parallelism": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queueName` | string | yes | The name of the queue. |
| `parallelism` | number | yes | Number of parallel consumers consuming from the queue. Default: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `POST /v2/queues` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-queue.md) for the provider-specific parameters and requirements.

