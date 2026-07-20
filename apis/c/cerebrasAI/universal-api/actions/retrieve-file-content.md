# Cerebras AI: Retrieve File Content

Retrieves file content from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-file-content?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-file-content?${params}`, {
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
| `fileId` | string | yes |  |

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
| `content` | string |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /v1/files/:fileId/content` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file-content.md) for the provider-specific parameters and requirements.

