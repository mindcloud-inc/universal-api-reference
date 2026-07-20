# Needle: Delete Files From Collection

Deletes files from a collection in Needle.

```
DELETE https://connect.mindcloud.co/v1/universal/needle/latest/actions/delete-files-from-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/needle/latest/actions/delete-files-from-collection?connectionId=$CONNECTION_ID&collectionId=string&file_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "file_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/delete-files-from-collection?${params}`, {
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
| `collectionId` | string | yes | ID of the collection to delete files from |
| `file_ids[]` | array<string> | yes | File IDs to remove from the collection |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Needle API returns.

## Native endpoint

Through the native Needle API, this operation is `DELETE /api/v1/collections/:collectionId/files` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files-from-collection.md) for the provider-specific parameters and requirements.

