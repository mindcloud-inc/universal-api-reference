# CraftMyPDF: Add watermark to a PDF

Adds a watermark to a PDF in CraftMyPDF.

```
PUT https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-watermark-to-apdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-watermark-to-apdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-watermark-to-apdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `text` | string | yes |  |
| `fontSize` | number | no |  |
| `opacity` | number | no |  |
| `rotation` | number | no |  |
| `hexColor` | string | no |  |
| `fontFamily` | string | no |  |
| `expiration` | number | no |  |
| `outputFile` | string | no |  |
| `cloudStorage` | number | no |  |
| `postactionS3Filekey` | string | no |  |
| `postactionS3Bucket` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string",
      "status": "string",
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
| `status` | string |  |
| `transactionRef` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /add-watermark` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-watermark-to-apdf.md) for the provider-specific parameters and requirements.

