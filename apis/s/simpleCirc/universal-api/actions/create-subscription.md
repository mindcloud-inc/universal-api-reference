# SimpleCirc: Create Subscription

Creates a subscription in SimpleCirc, or renews an existing one.

```
POST https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCirc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "publicationId": 1,
  "issuesPurchased": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "publicationId": 1,
    "issuesPurchased": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `publicationId` | number | yes |  |
| `issuesPurchased` | number | yes |  |
| `copies` | number | no |  |
| `postageId` | number | no |  |
| `promoCode` | string | no |  |
| `giftgiverAccountId` | string | no |  |
| `neverExpires` | boolean | no |  |
| `qualified` | boolean | no |  |
| `qualifiedOn` | date | no |  |
| `doNotRenew` | boolean | no |  |
| `amountPaid` | number | no |  |
| `amountDue` | number | no |  |
| `taxAmount` | number | no |  |
| `currency` | string | no |  |
| `questions` | object | no |  |

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
            "last_order": {},
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
| `subscriber.subscriptions[].last_order` | object |  |
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

Through the native SimpleCirc API, this operation is `POST /api/v1.2/subscribers/:account_id/subscriptions` (base URL `https://simplecirc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

