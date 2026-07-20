# Orq.ai: Delete File

Deletes an existing file from Orq.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/orqai/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=file_test_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "file_test_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | File ID from the Orq.ai path parameter. Example: `file_test_id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Orq.ai API returns.

## Native endpoint

Through the native Orq.ai API, this operation is `DELETE /v2/files/[:file_id]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

