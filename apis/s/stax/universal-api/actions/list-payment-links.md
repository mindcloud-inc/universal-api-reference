# Stax: List Payment Links

Retrieves payment links from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-payment-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-payment-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-payment-links?${params}`, {
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
      "active": true,
      "amount": 1,
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the payment link is active. |
| `amount` | number | Configured payment amount when fixed. |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Stax payment link identifier. |
| `name` | string | Payment link display name. |
| `updatedAt` | string | Last update timestamp. |
| `url` | string | Hosted payment link URL. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/payment-links` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-links.md) for the provider-specific parameters and requirements.

