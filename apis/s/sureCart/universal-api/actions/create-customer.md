# SureCart: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer.email": "customer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer.email": "customer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.email` | string | yes | The customer email address. Example: `customer@example.com`. |
| `customer.name` | string | no | The customer full name or business name. Example: `Test Customer`. |

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

Through the native SureCart API, this operation is `POST v1/customers` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

