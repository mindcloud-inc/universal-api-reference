# QStash: Delete Queue

Deletes an existing queue from QStash.

```
DELETE https://connect.mindcloud.co/v1/universal/qStash/latest/actions/delete-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/delete-queue?connectionId=$CONNECTION_ID&queueName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queueName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/delete-queue?${params}`, {
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
| `queueName` | string | yes | Name of the queue to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `DELETE /v2/queues/:queueName` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-queue.md) for the provider-specific parameters and requirements.

