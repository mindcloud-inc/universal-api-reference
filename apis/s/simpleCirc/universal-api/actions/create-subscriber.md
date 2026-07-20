# SimpleCirc: Create Subscriber

Creates a new subscriber in SimpleCirc.

```
POST https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCirc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `email` | string | no |  |
| `company` | string | no |  |
| `address1` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `state` | string | no |  |
| `zipcode` | string | no |  |
| `country` | string | no |  |
| `customFields` | object | no |  |

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
        "subscriptions": {},
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
| `subscriber.subscriptions` | object |  |
| `subscriber.title` | string |  |

## Native endpoint

Through the native SimpleCirc API, this operation is `POST /api/v1.2/subscribers` (base URL `https://simplecirc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber.md) for the provider-specific parameters and requirements.

