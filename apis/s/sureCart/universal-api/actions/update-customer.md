# SureCart: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "8fd47739-8749-4636-85b4-65ead1a58ee5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "8fd47739-8749-4636-85b4-65ead1a58ee5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The customer ID to update. Example: `8fd47739-8749-4636-85b4-65ead1a58ee5`. |
| `customer.name` | string | no | The updated customer full name or business name. Example: `Updated Customer`. |
| `cascadeDefaultPaymentMethod` | boolean | no | Cascade the default payment method to all subscriptions for this customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliationExpiresAt": 1,
      "billingAddress": "string",
      "billingMatchesShipping": true,
      "createdAt": 1,
      "defaultPaymentMethod": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "indexed": true,
      "lastName": "Chen",
      "liveMode": true,
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "portalUrl": "https://example.com",
      "shippingAddress": "string",
      "taxEnabled": true,
      "taxIdentifier": "string",
      "unsubscribed": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliationExpiresAt` | number |  |
| `billingAddress` | string |  |
| `billingMatchesShipping` | boolean |  |
| `createdAt` | number |  |
| `defaultPaymentMethod` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `indexed` | boolean |  |
| `lastName` | string |  |
| `liveMode` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `portalUrl` | string |  |
| `shippingAddress` | string |  |
| `taxEnabled` | boolean |  |
| `taxIdentifier` | string |  |
| `unsubscribed` | boolean |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `PATCH v1/customers/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

