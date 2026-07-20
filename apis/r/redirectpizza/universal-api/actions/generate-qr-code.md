# redirect.pizza: Generate QR Code



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/generate-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/generate-qr-code?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/generate-qr-code?${params}`, {
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
| `url` | string | yes | URL to encode into the QR code. |
| `format` | string | no | Output format. redirect.pizza documents png, svg, eps, and json with json as the default. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destination": "string",
      "filename": "Ava Chen",
      "image": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destination` | string |  |
| `filename` | string |  |
| `image` | string |  |
| `url` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/qr` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-qr-code.md) for the provider-specific parameters and requirements.

