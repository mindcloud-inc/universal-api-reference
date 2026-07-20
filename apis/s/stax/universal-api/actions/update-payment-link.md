# Stax: Update Payment Link

Updates or deactivates a payment link in Stax.

```
PUT https://connect.mindcloud.co/v1/universal/stax/latest/actions/update-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stax/latest/actions/update-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stax/latest/actions/update-payment-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Payment link identifier |

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

Through the native Stax API, this operation is `PUT /query/payment-links/:id` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-link.md) for the provider-specific parameters and requirements.

