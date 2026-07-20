# Plumsail Documents: Convert PPTX to PDF

Converts PPTX to PDF in Plumsail Documents.

```
POST https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-pptx-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-pptx-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-pptx-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no | PPTX file to upload. |
| `fileUrl` | string | no | Anonymous URL to a PPTX file. |
| `callbackUrl` | string | no | Webhook URL to receive async completion notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |

## Native endpoint

Through the native Plumsail Documents API, this operation is `POST /api/v2/convert/pptx-to-pdf` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pptx-to-pdf.md) for the provider-specific parameters and requirements.

