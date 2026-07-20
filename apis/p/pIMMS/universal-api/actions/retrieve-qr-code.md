# PIMMS: Retrieve QR Code

Retrieves a QR code image from PIMMS.

```
GET https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code?${params}`, {
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
| `url` | string | yes | The URL to generate a QR code for. |
| `logo` | string | no | The logo to include in the QR code. Can only be used with a paid plan on PiMMs |
| `size` | number | no | The size of the QR code in pixels. Defaults to `600` if not provided. |
| `level` | string | no | The level of error correction to use for the QR code. Defaults to `L` if not provided. |
| `fgColor` | string | no | The foreground color of the QR code in hex format. Defaults to `#000000` if not provided. |
| `bgColor` | string | no | The background color of the QR code in hex format. Defaults to `#ffffff` if not provided. |
| `hideLogo` | boolean | no | Whether to hide the logo in the QR code. Can only be used with a paid plan on PiMMs. |
| `margin` | number | no | The size of the margin around the QR code. Defaults to 2 if not provided. |
| `includeMargin` | boolean | no | DEPRECATED: Margin is included by default. Use the `margin` prop to customize the margin size. |

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
| `data` | array<number> | Raw PNG bytes surfaced as an array of numbers. |
| `type` | string | Node-style buffer discriminator returned for the raw PNG response. |

## Native endpoint

Through the native PIMMS API, this operation is `GET /qr` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-qr-code.md) for the provider-specific parameters and requirements.

