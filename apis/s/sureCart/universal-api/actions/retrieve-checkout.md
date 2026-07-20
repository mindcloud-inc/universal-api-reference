# SureCart: Retrieve Checkout



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-checkout?connectionId=$CONNECTION_ID&id=b7a1956e-2440-4a91-85bb-781f1c22dab7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "b7a1956e-2440-4a91-85bb-781f1c22dab7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-checkout?${params}`, {
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
| `id` | string | yes | The checkout ID to retrieve. Example: `b7a1956e-2440-4a91-85bb-781f1c22dab7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountDue": 1,
      "createdAt": 1,
      "currency": "string",
      "customer": "string",
      "email": "ava@example.com",
      "id": "string",
      "inheritedEmail": "ava@example.com",
      "inheritedName": "Ava Chen",
      "liveMode": true,
      "object": "string",
      "order": "string",
      "paymentMethodRequired": true,
      "portalUrl": "https://example.com",
      "remainingAmountDue": 1,
      "shippingEnabled": true,
      "status": "string",
      "subtotalAmount": 1,
      "taxAmount": 1,
      "taxEnabled": true,
      "totalAmount": 1,
      "totalSavingsAmount": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `email` | string |  |
| `id` | string |  |
| `inheritedEmail` | string |  |
| `inheritedName` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `order` | string |  |
| `paymentMethodRequired` | boolean |  |
| `portalUrl` | string |  |
| `remainingAmountDue` | number |  |
| `shippingEnabled` | boolean |  |
| `status` | string |  |
| `subtotalAmount` | number |  |
| `taxAmount` | number |  |
| `taxEnabled` | boolean |  |
| `totalAmount` | number |  |
| `totalSavingsAmount` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `GET v1/checkouts/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-checkout.md) for the provider-specific parameters and requirements.

