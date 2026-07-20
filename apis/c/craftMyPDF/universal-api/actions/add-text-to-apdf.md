# CraftMyPDF: Add text to a PDF

Adds text to a PDF in CraftMyPDF.

```
PUT https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-text-to-apdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-text-to-apdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "textSettings[]": [
    {}
  ],
  "textSettings[].pageSelector": "string",
  "textSettings[].text": "string",
  "textSettings[].position": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/add-text-to-apdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "textSettings[]": [{}],
    "textSettings[].pageSelector": "string",
    "textSettings[].text": "string",
    "textSettings[].position": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `textSettings[]` | array<object> | yes |  |
| `textSettings[].pageSelector` | string | yes |  |
| `textSettings[].text` | string | yes |  |
| `textSettings[].position` | string | yes |  |
| `textSettings[].offsetX` | number | no |  |
| `textSettings[].offsetY` | number | no |  |
| `textSettings[].fontSize` | number | no |  |
| `textSettings[].hexColor` | string | no |  |
| `textSettings[].fontFamily` | string | no |  |
| `textSettings[].opacity` | number | no |  |
| `textSettings[].rotation` | number | no |  |
| `expiration` | number | no |  |
| `outputFile` | string | no |  |
| `cloudStorage` | number | no |  |

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

Through the native CraftMyPDF API, this operation is `POST /add-text-to-pdf` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-text-to-apdf.md) for the provider-specific parameters and requirements.

