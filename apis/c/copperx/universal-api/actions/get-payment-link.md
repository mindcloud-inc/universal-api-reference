# Copperx: Get Payment Link

Retrieves a payment link from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-link?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-payment-link?${params}`, {
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

Through the native Copperx API, this operation is `GET /payment-links/{linkId}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-link.md) for the provider-specific parameters and requirements.

