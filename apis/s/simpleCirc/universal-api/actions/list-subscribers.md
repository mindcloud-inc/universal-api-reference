# SimpleCirc: List Subscribers

Retrieves a list of subscribers from SimpleCirc.

```
GET https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCirc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers?${params}`, {
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
| `limit` | number | no |  |
| `email` | string | no |  |
| `startingAfter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscribers": [
        {
          "account_id": "string",
          "address": {
            "address_1": "string",
            "address_2": "string",
            "city": "string",
            "country": "string",
            "state": "string",
            "zipcode": "string"
          },
          "company": "string",
          "custom_fields": {},
          "email": "ava@example.com",
          "first_name": "Ava",
          "last_name": "Chen",
          "login_link": "https://example.com",
          "name": "Ava Chen",
          "phone": "string",
          "renewal_link": "https://example.com",
          "subscriptions": [
            {
              "auto_renew": 1,
              "copies": 1,
              "digital_status": "string",
              "expiration_date": "string",
              "giftgiver": {},
              "issues_remaining": 1,
              "last_issue": 1,
              "last_order": {
                "amount_due": "string",
                "amount_paid": "string",
                "copies": 1,
                "custom_source": "string",
                "issues": "string",
                "never_expires": 1,
                "order_date_time": "string",
                "order_id": 1,
                "postage_type_id": 1,
                "price_description": "string",
                "promo_code": "string",
                "tax": "string"
              },
              "last_publish_date": "string",
              "last_volume": 1,
              "never_expires": 1,
              "postage_type_id": 1,
              "promo_code": "string",
              "publication_id": 1,
              "publication_name": "Ava Chen",
              "qualified": 1,
              "qualified_on": "string",
              "questions": {},
              "status": "string",
              "subscription_id": 1
            }
          ],
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscribers[].account_id` | string |  |
| `subscribers[].address.address_1` | string |  |
| `subscribers[].address.address_2` | string |  |
| `subscribers[].address.city` | string |  |
| `subscribers[].address.country` | string |  |
| `subscribers[].address.state` | string |  |
| `subscribers[].address.zipcode` | string |  |
| `subscribers[].company` | string |  |
| `subscribers[].custom_fields` | object |  |
| `subscribers[].email` | string |  |
| `subscribers[].first_name` | string |  |
| `subscribers[].last_name` | string |  |
| `subscribers[].login_link` | string |  |
| `subscribers[].name` | string |  |
| `subscribers[].phone` | string |  |
| `subscribers[].renewal_link` | string |  |
| `subscribers[].subscriptions[].auto_renew` | number |  |
| `subscribers[].subscriptions[].copies` | number |  |
| `subscribers[].subscriptions[].digital_status` | string |  |
| `subscribers[].subscriptions[].expiration_date` | string |  |
| `subscribers[].subscriptions[].giftgiver` | object |  |
| `subscribers[].subscriptions[].issues_remaining` | number |  |
| `subscribers[].subscriptions[].last_issue` | number |  |
| `subscribers[].subscriptions[].last_order.amount_due` | string |  |
| `subscribers[].subscriptions[].last_order.amount_paid` | string |  |
| `subscribers[].subscriptions[].last_order.copies` | number |  |
| `subscribers[].subscriptions[].last_order.custom_source` | string |  |
| `subscribers[].subscriptions[].last_order.issues` | string |  |
| `subscribers[].subscriptions[].last_order.never_expires` | number |  |
| `subscribers[].subscriptions[].last_order.order_date_time` | string |  |
| `subscribers[].subscriptions[].last_order.order_id` | number |  |
| `subscribers[].subscriptions[].last_order.postage_type_id` | number |  |
| `subscribers[].subscriptions[].last_order.price_description` | string |  |
| `subscribers[].subscriptions[].last_order.promo_code` | string |  |
| `subscribers[].subscriptions[].last_order.tax` | string |  |
| `subscribers[].subscriptions[].last_publish_date` | string |  |
| `subscribers[].subscriptions[].last_volume` | number |  |
| `subscribers[].subscriptions[].never_expires` | number |  |
| `subscribers[].subscriptions[].postage_type_id` | number |  |
| `subscribers[].subscriptions[].promo_code` | string |  |
| `subscribers[].subscriptions[].publication_id` | number |  |
| `subscribers[].subscriptions[].publication_name` | string |  |
| `subscribers[].subscriptions[].qualified` | number |  |
| `subscribers[].subscriptions[].qualified_on` | string |  |
| `subscribers[].subscriptions[].questions` | object |  |
| `subscribers[].subscriptions[].status` | string |  |
| `subscribers[].subscriptions[].subscription_id` | number |  |
| `subscribers[].title` | string |  |

## Native endpoint

Through the native SimpleCirc API, this operation is `GET /api/v1.2/subscribers` (base URL `https://simplecirc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

