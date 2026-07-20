# Verify550: Download Processed File

Downloads a processed file from Verify550.

```
GET https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-processed-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-processed-file?connectionId=$CONNECTION_ID&id=string&type=clean" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "type": "clean"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/download-processed-file?${params}`, {
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
| `id` | string | yes | Verify550 file identifier. |
| `type` | string | yes | Which processed result file to download. One of: `clean`, `full`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verify550 API returns.

## Native endpoint

Through the native Verify550 API, this operation is `GET /file` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-processed-file.md) for the provider-specific parameters and requirements.

