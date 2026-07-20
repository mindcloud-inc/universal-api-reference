# Copperx: Activate Payment Link

Activates a payment link in Copperx.

```
PUT https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-payment-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkId` | string | yes | Payment link ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "afterCompletion": "string",
      "allowedChains": [
        {}
      ],
      "allowPromotionCodes": true,
      "amount": "string",
      "billingAddressCollection": true,
      "createdAt": "string",
      "currencies": [
        "string"
      ],
      "currency": "string",
      "customFields": {},
      "description": "string",
      "emailCollection": true,
      "id": "string",
      "image": "string",
      "isActive": true,
      "nameCollection": true,
      "organizationId": "string",
      "phoneNumberCollection": true,
      "preferredCurrency": "string",
      "priceType": "string",
      "productId": "string",
      "shippingAddressCollection": true,
      "submitType": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `afterCompletion` | string |  |
| `allowedChains` | array<object> |  |
| `allowPromotionCodes` | boolean |  |
| `amount` | string |  |
| `billingAddressCollection` | boolean |  |
| `createdAt` | string |  |
| `currencies` | array<string> |  |
| `currency` | string |  |
| `customFields` | object |  |
| `description` | string |  |
| `emailCollection` | boolean |  |
| `id` | string |  |
| `image` | string |  |
| `isActive` | boolean |  |
| `nameCollection` | boolean |  |
| `organizationId` | string |  |
| `phoneNumberCollection` | boolean |  |
| `preferredCurrency` | string |  |
| `priceType` | string |  |
| `productId` | string |  |
| `shippingAddressCollection` | boolean |  |
| `submitType` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `POST /payment-links/{linkId}/activate` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-payment-link.md) for the provider-specific parameters and requirements.

