# Readwise: Update Reader Document

Updates an existing document in Readwise Reader.

```
PUT https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-reader-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-reader-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/update-reader-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The Readwise Reader document ID to update. |
| `title` | string | no | The document title to overwrite the current title. |
| `author` | string | no | The document author to overwrite the current author. |
| `summary` | string | no | Summary of the document. |
| `publishedDate` | string | no | Published datetime in ISO 8601 format. |
| `imageUrl` | string | no | Image URL to use as the cover image. |
| `seen` | boolean | no | Mark the document as seen or unseen. |
| `location` | string | no | Reader location for the document. |
| `category` | string | no | Reader category for the document. |
| `tags` | list<string> | no | List of tag strings to replace the current tags. |
| `notes` | string | no | Document note text. Pass an empty string to clear it. |

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

Through the native Readwise API, this operation is `PATCH /api/v3/update/:documentId/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reader-document.md) for the provider-specific parameters and requirements.

