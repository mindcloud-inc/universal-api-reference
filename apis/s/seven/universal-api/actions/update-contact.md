# Seven: Update Contact

Updates an existing contact in Seven.

```
PUT https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/update-contact', {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "groups": [
        1
      ],
      "id": 1,
      "initials": {
        "color": "string",
        "initials": "string"
      },
      "properties": {
        "address": "string",
        "birthday": "2026-05-07T12:00:00.000Z",
        "city": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "home_number": "string",
        "lastname": "Chen",
        "mobile_number": 1,
        "notes": "string",
        "postal_code": "string"
      },
      "validation": {
        "state": "string",
        "timestamp": "2026-05-07T12:00:00.000Z"
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
| `groups` | array<number> |  |
| `id` | number |  |
| `initials` | object |  |
| `initials.color` | string |  |
| `initials.initials` | string |  |
| `properties` | object |  |
| `properties.address` | string |  |
| `properties.birthday` | date |  |
| `properties.city` | string |  |
| `properties.email` | string |  |
| `properties.firstname` | string |  |
| `properties.home_number` | string |  |
| `properties.lastname` | string |  |
| `properties.mobile_number` | number |  |
| `properties.notes` | string |  |
| `properties.postal_code` | string |  |
| `validation` | object |  |
| `validation.state` | string |  |
| `validation.timestamp` | date |  |

## Native endpoint

Through the native Seven API, this operation is `PATCH /contacts/:id` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

