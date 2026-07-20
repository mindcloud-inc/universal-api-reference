# Image-Charts: Create QR Code

Creates a QR code image with Image-Charts.

```
GET https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Image-Charts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-qr-code?connectionId=$CONNECTION_ID&size=string&content=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "size": "string",
  "content": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-qr-code?${params}`, {
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
| `size` | string | yes | Image size in pixels as widthxheight, for example 150x150. |
| `content` | string | yes | Text or URL to encode in the QR code. |
| `characterEncoding` | string | no | Character encoding used for QR payload text. Default: `UTF-8`. |

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
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Image-Charts API, this operation is `GET /chart` (base URL `https://image-charts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.

