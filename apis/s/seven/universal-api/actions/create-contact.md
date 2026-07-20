# Seven: Create Contact

Creates a new contact in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "groups": [
        "string"
      ],
      "id": 1,
      "initials": {
        "color": "string",
        "initials": "string"
      },
      "properties": {
        "address": "string",
        "birthday": "string",
        "city": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "home_number": "string",
        "lastname": "Chen",
        "mobile_number": "string",
        "notes": "string",
        "postal_code": "string"
      },
      "validation": {
        "state": "string",
        "timestamp": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `created` | date |  |
| `groups` | array<string> |  |
| `id` | number |  |
| `initials` | object |  |
| `initials.color` | string |  |
| `initials.initials` | string |  |
| `properties` | object |  |
| `properties.address` | string |  |
| `properties.birthday` | string |  |
| `properties.city` | string |  |
| `properties.email` | string |  |
| `properties.firstname` | string |  |
| `properties.home_number` | string |  |
| `properties.lastname` | string |  |
| `properties.mobile_number` | string |  |
| `properties.notes` | string |  |
| `properties.postal_code` | string |  |
| `validation` | object |  |
| `validation.state` | string |  |
| `validation.timestamp` | string |  |

## Native endpoint

Through the native Seven API, this operation is `POST /contacts` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

