# Mem0: Batch Delete Memories

Deletes multiple memories from Mem0.

```
DELETE https://connect.mindcloud.co/v1/universal/mem0/latest/actions/batch-delete-memories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/batch-delete-memories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/batch-delete-memories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Mem0 API, this operation is `DELETE /v1/batch/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-memories.md) for the provider-specific parameters and requirements.

