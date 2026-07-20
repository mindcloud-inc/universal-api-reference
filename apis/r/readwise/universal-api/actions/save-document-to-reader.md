# Readwise: Save Document To Reader

Saves a document to Readwise Reader.

```
POST https://connect.mindcloud.co/v1/universal/readwise/latest/actions/save-document-to-reader
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/save-document-to-reader" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/save-document-to-reader', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The document's unique URL. |
| `html` | string | no | The document content in valid HTML. |
| `should_clean_html` | boolean | no | Automatically clean provided HTML and parse metadata. |
| `title` | string | no | Override title for the document. |
| `author` | string | no | Override author for the document. |
| `summary` | string | no | Summary of the document. |
| `published_date` | date | no | ISO 8601 datetime when the document was published. |
| `image_url` | string | no | Cover image URL for the document. |
| `location` | string | no | Initial location for the document. |
| `category` | string | no | Category for the saved document. |
| `saved_using` | string | no | Source of the document. |
| `tags[]` | array<string> | no | List of tag strings for the document. |
| `notes` | string | no | Top-level note for the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `POST /api/v3/save/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-document-to-reader.md) for the provider-specific parameters and requirements.

