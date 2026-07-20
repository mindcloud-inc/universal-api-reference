# Orq.ai: Download File Content

Retrieves a presigned file download URL from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/download-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/download-file-content?connectionId=$CONNECTION_ID&fileIdOrPath=file_test_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileIdOrPath": "file_test_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/download-file-content?${params}`, {
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
| `fileIdOrPath` | string | yes | File ID or Path from the Orq.ai path parameter. Example: `file_test_id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Orq.ai API returns.

## Native endpoint

Through the native Orq.ai API, this operation is `GET /v2/files/[:file_id_or_path]/content` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file-content.md) for the provider-specific parameters and requirements.

