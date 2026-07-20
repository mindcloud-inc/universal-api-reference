# CraftMyPDF: Create PDF from templates

Creates a PDF from templates in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pdf-from-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pdf-from-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templates[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-pdf-from-templates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templates[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templates[]` | array<object> | yes |  |
| `data` | object | no |  |
| `exportType` | string | no |  |
| `expiration` | number | no |  |
| `outputFile` | string | no |  |
| `paging` | string | no |  |
| `cloudStorage` | number | no |  |
| `postactionS3Filekey` | string | no |  |
| `postactionS3Bucket` | string | no |  |
| `imageResampleRes` | number | no |  |
| `resizeImages` | boolean | no |  |
| `resizeMaxWidth` | number | no |  |
| `resizeMaxHeight` | number | no |  |
| `resizeFormat` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string",
      "fileSize": 1,
      "status": "string",
      "totalPages": 1,
      "transactionRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string |  |
| `fileSize` | number |  |
| `status` | string |  |
| `totalPages` | number |  |
| `transactionRef` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /create-merge` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-templates.md) for the provider-specific parameters and requirements.

