# Plumsail Documents: Create DOCX Document

Creates a DOCX document in Plumsail Documents.

```
POST https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/create-docx-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/create-docx-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/create-docx-document', {
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
| `locale` | string | no | Locale used to format dates, numbers, and currencies in the output document. |
| `data` | string | no | JSON object with values to merge into the DOCX template. |
| `outputType` | string | no | Optional output format for the generated document. |
| `timezone` | string | no | IANA timezone used for date tokens and date formatting. |
| `engine` | string | no | Template engine to use for DOCX processing. |
| `file` | file | no | DOCX template file to upload. |
| `fileUrl` | string | no | Anonymous URL to a DOCX template file. |
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

Through the native Plumsail Documents API, this operation is `POST /api/v2/generate/from-docx` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-docx-document.md) for the provider-specific parameters and requirements.

