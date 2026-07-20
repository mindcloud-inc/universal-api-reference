# LogMeIn: Find Related Documents By Text

Finds related knowledge base documents in LogMeIn by text.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents-by-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents-by-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents-by-text?${params}`, {
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
| `text` | string | yes | Required text to find semantically related documents for. |
| `limit` | number | no | Maximum number of related documents to return. |
| `minScore` | number | no | Minimum relevance score between 0 and 1. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Comma-separated tenant IDs to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "score": 1,
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `score` | number |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /resolve/knowledge-base/v2/documents/related` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-related-documents-by-text.md) for the provider-specific parameters and requirements.

