# CustomGPT.ai: Get Document Metadata

Retrieves document metadata from a CustomGPT.ai agent.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-document-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-document-metadata?connectionId=$CONNECTION_ID&projectId=1&pageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "pageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-document-metadata?${params}`, {
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
| `projectId` | number | yes | The project ID of the agent. |
| `pageId` | number | yes | The document page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "image": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `image` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `GET /projects/:projectId/pages/:pageId/metadata` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-metadata.md) for the provider-specific parameters and requirements.

