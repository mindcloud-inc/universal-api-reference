# Libraria: Add Document

Add a new document to your library via scraping or raw text.

```
POST https://connect.mindcloud.co/v1/universal/libraria/latest/actions/add-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Libraria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "libraryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/libraria/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "libraryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `libraryId` | string | yes | The ID of the library to add the document to. |
| `url` | string | no | A URL to scrape into the library. |
| `text` | string | no | A raw text document to add to the library. |
| `title` | string | no | The title to use for a raw text document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | no | The source URL used for the Learn More snippet. |
| `imageSnippet` | string | no | The image URL to attach as the document snippet. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing document ingestion result. |
| `status` | string | Libraria create-document result status. |

## Native endpoint

Through the native Libraria API, this operation is `POST /library/:library_id/document` (base URL `https://api.libraria.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document.md) for the provider-specific parameters and requirements.

