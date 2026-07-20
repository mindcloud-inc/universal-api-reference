# Open AI: Get File Content

Retrieves file contents from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file-content?connectionId=$CONNECTION_ID&file_id=file-9iKAYkbraQ7QHGmqhYnapo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "file-9iKAYkbraQ7QHGmqhYnapo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/get-file-content?${params}`, {
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
| `file_id` | string | yes | OpenAI file ID whose content to download. Default: `file-9iKAYkbraQ7QHGmqhYnapo`. |

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
| `content` | string | Raw file content. |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/files/:file_id/content` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-content.md) for the provider-specific parameters and requirements.

