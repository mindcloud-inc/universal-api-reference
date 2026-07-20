# More Good Reviews: Create or Update Customer

Creates a customer in More Good Reviews.

```
POST https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a More Good Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/create-or-update-customer', {
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
| `hasSubscription` | boolean | no | Whether the customer is subscribed to your service. |
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
      "address1": "string",
      "address2": "string",
      "charges_avg": 1,
      "charges_count": 1,
      "charges_sum": 1,
      "city": "string",
      "color": "string",
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_asked_at": 1,
      "first_charged_at": 1,
      "first_name": "Ava",
      "gravatar": "string",
      "has_subscription": 1,
      "id": 1,
      "is_validated": true,
      "lang": "string",
      "last_asked_at": 1,
      "last_charged_at": 1,
      "last_name": "Chen",
      "location_id": 1,
      "location": {
        "address": "string",
        "address1": "string",
        "address2": "string",
        "city": "string",
        "code": "string",
        "display_name": "Ava Chen",
        "id": 1,
        "name": "Ava Chen",
        "postal_code": "string",
        "project_id": 1,
        "slug": "string",
        "state": "string",
        "title": "string",
        "uuid": "string"
      },
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "phone_e164": "string",
      "phone_formatted": "string",
      "postal_code": "string",
      "review_link": "https://example.com",
      "signed_up_at": 1,
      "state": "string",
      "unsubscribe_link": "https://example.com",
      "updated_at": 1,
      "uuid": "string",
      "validation": {
        "address": "string",
        "engagement": {
          "engaging": true,
          "is_bot": true
        },
        "is_disposable_address": true,
        "is_role_address": true,
        "reason": [
          "string"
        ],
        "result": "string",
        "risk": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `charges_avg` | number |  |
| `charges_count` | number |  |
| `charges_sum` | number |  |
| `city` | string |  |
| `color` | string |  |
| `company` | string |  |
| `created_at` | number |  |
| `email` | string |  |
| `first_asked_at` | number |  |
| `first_charged_at` | number |  |
| `first_name` | string |  |
| `gravatar` | string |  |
| `has_subscription` | number |  |
| `id` | number |  |
| `is_validated` | boolean |  |
| `lang` | string |  |
| `last_asked_at` | number |  |
| `last_charged_at` | number |  |
| `last_name` | string |  |
| `location_id` | number |  |
| `location.address` | string |  |
| `location.address1` | string |  |
| `location.address2` | string |  |
| `location.city` | string |  |
| `location.code` | string |  |
| `location.display_name` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.postal_code` | string |  |
| `location.project_id` | number |  |
| `location.slug` | string |  |
| `location.state` | string |  |
| `location.title` | string |  |
| `location.uuid` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `phone_e164` | string |  |
| `phone_formatted` | string |  |
| `postal_code` | string |  |
| `review_link` | string |  |
| `signed_up_at` | number |  |
| `state` | string |  |
| `unsubscribe_link` | string |  |
| `updated_at` | number |  |
| `uuid` | string |  |
| `validation.address` | string |  |
| `validation.engagement.engaging` | boolean |  |
| `validation.engagement.is_bot` | boolean |  |
| `validation.is_disposable_address` | boolean |  |
| `validation.is_role_address` | boolean |  |
| `validation.reason[]` | string |  |
| `validation.result` | string |  |
| `validation.risk` | string |  |

## Native endpoint

Through the native More Good Reviews API, this operation is `POST /beacon/customers` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

