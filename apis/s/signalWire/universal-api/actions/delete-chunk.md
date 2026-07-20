# SignalWire: Delete Chunk

Deletes an existing chunk from SignalWire.

```
DELETE https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-chunk?connectionId=$CONNECTION_ID&documentId=string&chunkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "chunkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-chunk?${params}`, {
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
| `documentId` | string | yes | Unique ID of the parent Document. |
| `chunkId` | string | yes | Unique ID of a Chunk. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignalWire API returns.

## Native endpoint

Through the native SignalWire API, this operation is `DELETE /datasphere/documents/{documentId}/chunks/{chunkId}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-chunk.md) for the provider-specific parameters and requirements.

