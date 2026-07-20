# Wikibot: Upload Knowledge Base Document

Uploads a knowledge base document to Wikibot.

```
POST https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/upload-knowledge-base-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/upload-knowledge-base-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/upload-knowledge-base-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | PDF or DOCX file to upload to the knowledge base. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | number | Uploaded file identifier. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/kb/upload-file` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-knowledge-base-document.md) for the provider-specific parameters and requirements.

