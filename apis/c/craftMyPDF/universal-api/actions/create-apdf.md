# CraftMyPDF: Create a PDF

Creates a PDF document in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `data` | object | yes |  |
| `loadDataFrom` | string | no |  |
| `version` | string | no |  |
| `exportType` | string | no |  |
| `expiration` | number | no |  |
| `outputFile` | string | no |  |
| `imageResampleRes` | number | no |  |
| `directDownload` | number | no |  |
| `cloudStorage` | number | no |  |
| `passwordProtected` | boolean | no |  |
| `password` | string | no |  |
| `postactionS3Filekey` | string | no |  |
| `postactionS3Bucket` | string | no |  |
| `resizeImages` | boolean | no |  |
| `resizeMaxWidth` | number | no |  |
| `resizeMaxHeight` | number | no |  |
| `resizeFormat` | string | no |  |
| `paging` | string | no |  |
| `pdfVersion` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string",
      "fileSize": 1,
      "status": "string",
      "templateId": "string",
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
| `templateId` | string |  |
| `totalPages` | number |  |
| `transactionRef` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /create` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-apdf.md) for the provider-specific parameters and requirements.

