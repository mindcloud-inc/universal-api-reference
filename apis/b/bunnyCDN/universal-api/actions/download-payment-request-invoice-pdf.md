# BunnyCDN: Download Payment Request Invoice PDF

Retrieves a BunnyCDN payment request invoice PDF.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/download-payment-request-invoice-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/download-payment-request-invoice-pdf?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/download-payment-request-invoice-pdf?${params}`, {
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
| `id` | string | yes | The Bunny payment request identifier. |

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
| `data` | string | Raw PDF response body or empty body from Bunny billing invoice download endpoint. |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /billing/payment-request-invoice/:id/pdf` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-payment-request-invoice-pdf.md) for the provider-specific parameters and requirements.

