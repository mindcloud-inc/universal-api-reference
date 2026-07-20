# SimpleCirc: Create or Update Address

Creates or updates a subscriber address in SimpleCirc.

```
POST https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-or-update-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCirc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-or-update-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "address1": "string",
  "city": "string",
  "state": "string",
  "zipcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-or-update-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "address1": "string",
    "city": "string",
    "state": "string",
    "zipcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `address1` | string | yes |  |
| `address2` | string | no |  |
| `city` | string | yes |  |
| `state` | string | yes |  |
| `zipcode` | string | yes |  |
| `country` | string | no |  |

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
| `subscriber.title` | string |  |

## Native endpoint

Through the native SimpleCirc API, this operation is `POST /api/v1.2/subscribers/:account_id/addresses` (base URL `https://simplecirc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-address.md) for the provider-specific parameters and requirements.

