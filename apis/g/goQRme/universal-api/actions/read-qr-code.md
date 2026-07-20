# goQR.me: Read QR Code

Reads a QR code with goQR.me.

```
GET https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a goQR.me `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code?${params}`, {
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
| `fileurl` | string | no | URL of a publicly reachable QR code image. Example: `https://example.com/qr-code.png`. |
| `file` | file | no | Upload a QR code image file. |
| `outputformat` | list<string> | no | Response format for the scan result. One of: `JSON`, `XML`. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "symbol": [
        {
          "data": "string",
          "error": "string",
          "seq": 1
        }
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
| `symbol[].data` | string |  |
| `symbol[].error` | string |  |
| `symbol[].seq` | number |  |
| `type` | string |  |

## Native endpoint

Through the native goQR.me API, this operation is `POST /read-qr-code/` (base URL `https://api.qrserver.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-qr-code.md) for the provider-specific parameters and requirements.

