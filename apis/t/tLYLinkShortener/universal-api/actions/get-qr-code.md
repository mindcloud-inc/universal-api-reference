# TLY Link Shortener: Get QR Code

Retrieves a QR code from TLY Link Shortener.

```
GET https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-qr-code?${params}`, {
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
| `shortUrl` | string | yes | The short URL to generate the QR code for. |
| `output` | string | no | Optional response format such as image or base64. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64` | string |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `GET /api/v1/link/qr-code` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.

