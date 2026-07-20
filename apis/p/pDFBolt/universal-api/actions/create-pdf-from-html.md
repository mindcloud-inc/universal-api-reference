# PDFBolt: Create PDF from HTML

Creates a PDF from HTML in PDFBolt.

```
POST https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-from-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFBolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/create-pdf-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Base64-encoded HTML content to convert into a PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native PDFBolt API, this operation is `POST /direct` (base URL `https://api.pdfbolt.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-html.md) for the provider-specific parameters and requirements.

