# SimpleCirc: Retrieve Subscriber

Retrieves details for a subscriber from SimpleCirc.

```
GET https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/retrieve-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCirc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/retrieve-subscriber?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/retrieve-subscriber?${params}`, {
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
| `accountId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber.account_id` | string |  |
| `subscriber.address.address_1` | string |  |
| `subscriber.address.address_2` | string |  |
| `subscriber.address.city` | string |  |
| `subscriber.address.country` | string |  |
| `subscriber.address.state` | string |  |
| `subscriber.address.zipcode` | string |  |
| `subscriber.company` | string |  |
| `subscriber.custom_fields` | object |  |
| `subscriber.email` | string |  |
| `subscriber.first_name` | string |  |
| `subscriber.last_name` | string |  |
| `subscriber.login_link` | string |  |
| `subscriber.name` | string |  |
| `subscriber.phone` | string |  |
| `subscriber.renewal_link` | string |  |
| `subscriber.subscriptions[].auto_renew` | number |  |
| `subscriber.subscriptions[].copies` | number |  |
| `subscriber.subscriptions[].digital_status` | string |  |
| `subscriber.subscriptions[].expiration_date` | string |  |
| `subscriber.subscriptions[].giftgiver` | object |  |
| `subscriber.subscriptions[].issues_remaining` | number |  |
| `subscriber.subscriptions[].last_issue` | number |  |
| `subscriber.subscriptions[].last_order.amount_due` | string |  |
| `subscriber.subscriptions[].last_order.amount_paid` | string |  |
| `subscriber.subscriptions[].last_order.copies` | number |  |
| `subscriber.subscriptions[].last_order.custom_source` | string |  |
| `subscriber.subscriptions[].last_order.issues` | string |  |
| `subscriber.subscriptions[].last_order.never_expires` | number |  |
| `subscriber.subscriptions[].last_order.order_date_time` | string |  |
| `subscriber.subscriptions[].last_order.order_id` | number |  |
| `subscriber.subscriptions[].last_order.postage_type_id` | number |  |
| `subscriber.subscriptions[].last_order.price_description` | string |  |
| `subscriber.subscriptions[].last_order.promo_code` | string |  |
| `subscriber.subscriptions[].last_order.tax` | string |  |
| `subscriber.subscriptions[].last_publish_date` | string |  |
| `subscriber.subscriptions[].last_volume` | number |  |
| `subscriber.subscriptions[].never_expires` | number |  |
| `subscriber.subscriptions[].postage_type_id` | number |  |
| `subscriber.subscriptions[].promo_code` | string |  |
| `subscriber.subscriptions[].publication_id` | number |  |
| `subscriber.subscriptions[].publication_name` | string |  |
| `subscriber.subscriptions[].qualified` | number |  |
| `subscriber.subscriptions[].qualified_on` | string |  |
| `subscriber.subscriptions[].questions` | object |  |
| `subscriber.subscriptions[].status` | string |  |
| `subscriber.subscriptions[].subscription_id` | number |  |
| `subscriber.title` | string |  |

## Native endpoint

Through the native SimpleCirc API, this operation is `GET /api/v1.2/subscribers/:account_id` (base URL `https://simplecirc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscriber.md) for the provider-specific parameters and requirements.

