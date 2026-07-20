# Formstack Documents: List Documents

Retrieves a list of documents from Formstack Documents.

```
GET https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents?${params}`, {
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
| `folder` | string | no | Return documents in this folder name. |
| `search` | string | no | Return documents matching this search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "output": "string",
      "size": "string",
      "sizeHeight": "string",
      "sizeWidth": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `output` | string |  |
| `size` | string |  |
| `sizeHeight` | string |  |
| `sizeWidth` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `GET /documents` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

