# Seven: Get Contact

Retrieves a contact from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-contact?${params}`, {
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

Through the native Seven API, this operation is `GET /contacts/:id` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

