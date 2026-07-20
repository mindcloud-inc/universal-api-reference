# Skribble Sign: Create Document

Creates a new document in Skribble Sign.

```
POST https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | The document title. |
| `content` | string | yes | The base64 encoded PDF content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "page_count": 1,
      "size": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string | Document MIME type. |
| `created_at` | date | Creation timestamp. |
| `id` | string | Document ID. |
| `page_count` | number | Number of document pages. |
| `size` | number | Document size in bytes. |
| `title` | string | Document title. |

## Native endpoint

Through the native Skribble Sign API, this operation is `POST /v2/documents` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

