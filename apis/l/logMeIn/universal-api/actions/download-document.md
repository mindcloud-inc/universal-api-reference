# LogMeIn: Download Document

Downloads a knowledge base document from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/download-document?${params}`, {
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
| `documentId` | string | yes | Required document ID. |
| `inline` | boolean | no | Whether to display the file inline instead of downloading. |
| `draft` | boolean | no | Whether to download the draft version instead of the published document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileName": "Ava Chen",
      "id": "string",
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
| `contentType` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/documents/:documentId/download` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-document.md) for the provider-specific parameters and requirements.

