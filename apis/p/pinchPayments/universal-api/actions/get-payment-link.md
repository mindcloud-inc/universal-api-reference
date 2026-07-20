# Pinch Payments: Get Payment Link

Retrieves a payment link from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payment-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payment-link?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /payment-links/[:id]` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-link.md) for the provider-specific parameters and requirements.

