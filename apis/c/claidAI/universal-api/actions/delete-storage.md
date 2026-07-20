# Claid AI: Delete Storage

Deletes a storage connector from Claid AI by storage ID.

```
DELETE https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/delete-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/delete-storage?connectionId=$CONNECTION_ID&storageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/delete-storage?${params}`, {
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
| `storageId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Claid AI API returns.

## Native endpoint

Through the native Claid AI API, this operation is `DELETE storage/storages/:storage_id` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-storage.md) for the provider-specific parameters and requirements.

