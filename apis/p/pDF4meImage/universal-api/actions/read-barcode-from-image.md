# PDF4me Image: Read Barcode from Image

Retrieves barcode data from an image in PDF4me Image.

```
GET https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/read-barcode-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF4me Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/read-barcode-from-image?connectionId=$CONNECTION_ID&docContent=string&docName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docContent": "string",
  "docName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/read-barcode-from-image?${params}`, {
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
| `docContent` | string | yes | Base64-encoded source image content. |
| `docName` | string | yes | Filename for the source image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "jobId": "string",
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string | Decoded barcode or QR code value. |
| `jobId` | string | Provider job identifier when available. |
| `traceId` | string | Provider trace identifier for the scan request. |

## Native endpoint

Through the native PDF4me Image API, this operation is `POST /ReadBarcodesfromImage` (base URL `https://api.pdf4me.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-barcode-from-image.md) for the provider-specific parameters and requirements.

