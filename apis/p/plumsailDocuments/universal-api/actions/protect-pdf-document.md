# Plumsail Documents: Protect PDF Document

Protects a PDF document in Plumsail Documents.

```
POST https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/protect-pdf-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/protect-pdf-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowPrinting": true,
  "allowModification": true,
  "allowExtract": true,
  "allowAnnotate": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/protect-pdf-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowPrinting": true,
    "allowModification": true,
    "allowExtract": true,
    "allowAnnotate": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowPrinting` | boolean | yes |  |
| `allowModification` | boolean | yes |  |
| `allowExtract` | boolean | yes |  |
| `allowAnnotate` | boolean | yes |  |
| `newOwnerPassword` | string | no |  |
| `newUserPassword` | string | no |  |
| `password` | string | no |  |
| `file` | file | no |  |
| `fileUrl` | string | no |  |
| `callbackUrl` | string | no |  |

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

Through the native Plumsail Documents API, this operation is `POST /api/v2/pdf/protect` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/protect-pdf-document.md) for the provider-specific parameters and requirements.

