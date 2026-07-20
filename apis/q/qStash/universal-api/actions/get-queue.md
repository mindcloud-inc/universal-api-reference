# QStash: Get Queue

Retrieves a queue from QStash by name.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-queue?connectionId=$CONNECTION_ID&queueName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queueName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-queue?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queueName` | string | yes | Name of the queue to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "lag": 1,
      "name": "Ava Chen",
      "parallelism": 1,
      "paused": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `lag` | number |  |
| `name` | string |  |
| `parallelism` | number |  |
| `paused` | boolean |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/queues/:queueName` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue.md) for the provider-specific parameters and requirements.

