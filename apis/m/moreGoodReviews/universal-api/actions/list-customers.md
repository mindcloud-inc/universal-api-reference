# More Good Reviews: List Customers

Retrieves customers from More Good Reviews.

```
GET https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a More Good Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native More Good Reviews API, this operation is `GET /beacon/customers` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

