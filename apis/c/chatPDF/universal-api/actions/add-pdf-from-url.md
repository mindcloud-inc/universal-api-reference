# ChatPDF: Add PDF From URL



```
POST https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/add-pdf-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/add-pdf-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/file.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/add-pdf-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/file.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Publicly accessible URL of the PDF file to add. Example: `https://example.com/file.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sourceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sourceId` | string | ChatPDF source ID created from the URL import. |

## Native endpoint

Through the native ChatPDF API, this operation is `POST /sources/add-url` (base URL `https://api.chatpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-pdf-from-url.md) for the provider-specific parameters and requirements.

