# Open AI: Get File

Retrieves a file from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file?connectionId=$CONNECTION_ID&file_id=file-9iKAYkbraQ7QHGmqhYnapo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "file-9iKAYkbraQ7QHGmqhYnapo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file?${params}`, {
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
| `file_id` | string | yes | OpenAI file ID to retrieve. Default: `file-9iKAYkbraQ7QHGmqhYnapo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "created_at": 1,
      "expires_at": 1,
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string",
      "status": "string",
      "status_details": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number | File size in bytes. |
| `created_at` | number | Creation timestamp. |
| `expires_at` | number | Expiry timestamp. |
| `filename` | string | Filename. |
| `id` | string | File ID. |
| `object` | string | Object type. |
| `purpose` | string | File purpose. |
| `status` | string | Processing status. |
| `status_details` | object | Additional status details. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/files/:file_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

