# SureCart: Create Checkout



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkout.email": "customer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkout.email": "customer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkout.email` | string | yes | The customer email used for the checkout. Example: `customer@example.com`. |

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

Through the native SureCart API, this operation is `POST v1/checkouts` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout.md) for the provider-specific parameters and requirements.

