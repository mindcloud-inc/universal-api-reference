# xAI: Download File Content

Downloads file content from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/download-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/download-file-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/download-file-content?${params}`, {
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
| `file_id` | string | no | File identifier whose content should be downloaded. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | File content returned by text downloads or binary placeholder for clients. |

## Native endpoint

Through the native xAI API, this operation is `GET /files/:file_id/content` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file-content.md) for the provider-specific parameters and requirements.

