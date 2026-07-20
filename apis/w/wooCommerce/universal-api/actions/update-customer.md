# WooCommerce: Update Customer

Updates an existing customer in WooCommerce.

```
PUT https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<number> | yes | Unique numeric ID of the customer to update. |
| `email` | string | no | Customer email address. |
| `firstName` | string | no | Customer first name. |
| `lastName` | string | no | Customer last name. |
| `username` | string | no | Customer username. |
| `password` | string | no | Customer password. |
| `billing` | object | no |  |
| `billing.firstName` | string | no |  |
| `billing.lastName` | string | no |  |
| `billing.company` | string | no |  |
| `billing.address1` | string | no |  |
| `billing.address2` | string | no |  |
| `billing.city` | string | no |  |
| `billing.state` | string | no |  |
| `billing.postcode` | string | no |  |
| `billing.country` | string | no |  |
| `billing.email` | string | no |  |
| `billing.phone` | string | no |  |
| `shipping` | object | no |  |
| `shipping.firstName` | string | no |  |
| `shipping.lastName` | string | no |  |
| `shipping.company` | string | no |  |
| `shipping.address1` | string | no |  |
| `shipping.address2` | string | no |  |
| `shipping.city` | string | no |  |
| `shipping.state` | string | no |  |
| `shipping.postcode` | string | no |  |
| `shipping.country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "billing": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isPayingCustomer": true,
      "lastName": "Chen",
      "metaData": [
        {}
      ],
      "role": "string",
      "shipping": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `billing` | object |  |
| `dateCreated` | date |  |
| `dateCreatedGmt` | date |  |
| `dateModified` | date |  |
| `dateModifiedGmt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isPayingCustomer` | boolean |  |
| `lastName` | string |  |
| `metaData` | array<object> |  |
| `role` | string |  |
| `shipping` | object |  |
| `username` | string |  |

## Native endpoint

Through the native WooCommerce API, this operation is `PUT /customers/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

