# Fintoc: List Payment Links

Retrieves payment links from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-links?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "checkout": {},
      "created_at": "string",
      "currency": "string",
      "customer_email": "ava@example.com",
      "expires_at": "string",
      "id": "string",
      "metadata": {},
      "mode": "string",
      "object": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `checkout` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer_email` | string |  |
| `expires_at` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `object` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v1/payment_links` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-links.md) for the provider-specific parameters and requirements.

