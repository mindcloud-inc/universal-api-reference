# PDF.co: Read Barcodes

Reads barcodes from a file in PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/read-barcodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/read-barcodes?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fbarcode.png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/barcode.png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/read-barcodes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of image or PDF containing barcodes. Example: `https://example.com/barcode.png`. |
| `types` | string | no | Optional list of barcode types to detect. Example: `Code128`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcodes": [
        {}
      ],
      "credits": 1,
      "duration": 1,
      "error": true,
      "pageCount": 1,
      "remainingCredits": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcodes` | array<object> |  |
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | number |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /barcode/read/from/url` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-barcodes.md) for the provider-specific parameters and requirements.

