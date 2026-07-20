# Florm: Get Form QR Code

Retrieves a QR code for a Florm form.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-qr-code?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-qr-code?${params}`, {
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
| `url` | string | yes | Public form URL to encode into the QR code image. |
| `download` | boolean | no | Set true to force a downloadable QR code response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Binary PNG payload returned by Florm for the generated QR code. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/forms/qrcode` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-qr-code.md) for the provider-specific parameters and requirements.

