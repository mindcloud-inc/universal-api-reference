# Saastic: Create or Update Customer

Creates or updates a customer in Saastic.

```
POST https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-or-update-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | The customer's first name. |
| `lastName` | string | no | The customer's last name. |
| `email` | string | no | The customer's email address. |
| `phone` | string | no | The customer's phone number. |
| `company` | string | no | The customer's company name. |
| `signedUpAt` | date | no | The date the customer signed up to your service. |
| `hasSubscription` | boolean | no | Whether or not the customer is subscribed to your service. |
| `locationSlug` | string | no | The slug of a location. |
| `notes` | string | no | Notes for internal use only. |
| `tags[]` | array<string> | no | An array of customer tag slugs to apply to the customer. |
| `address1` | string | no | The customer's address line 1. |
| `address2` | string | no | The customer's address line 2. |
| `city` | string | no | The customer's city or town. |
| `state` | string | no | The customer's state or region. |
| `postalCode` | string | no | The customer's postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "has_subscription": 1,
      "id": 1,
      "last_name": "Chen",
      "location_id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "review_link": "https://example.com",
      "updated_at": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `created_at` | number |  |
| `email` | string |  |
| `first_name` | string |  |
| `has_subscription` | number |  |
| `id` | number |  |
| `last_name` | string |  |
| `location_id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `review_link` | string |  |
| `updated_at` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `POST /beacon/customers` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

