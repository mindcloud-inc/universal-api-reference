# Gorgias: Retrieve User

Retrieves a user from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-user?${params}`, {
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
| `id` | string | yes | User ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "bio": "string",
      "client_id": "string",
      "country": "string",
      "created_datetime": "string",
      "deactivated_datetime": "string",
      "email": "ava@example.com",
      "external_id": "string",
      "firstname": "Ava",
      "has_2fa_enabled": true,
      "has_password": true,
      "id": 1,
      "language": "string",
      "lastname": "Chen",
      "meta": {},
      "name": "Ava Chen",
      "role": {},
      "timezone": "string",
      "updated_datetime": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `bio` | string |  |
| `client_id` | string |  |
| `country` | string |  |
| `created_datetime` | string |  |
| `deactivated_datetime` | string |  |
| `email` | string |  |
| `external_id` | string |  |
| `firstname` | string |  |
| `has_2fa_enabled` | boolean |  |
| `has_password` | boolean |  |
| `id` | number |  |
| `language` | string |  |
| `lastname` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `role` | object |  |
| `timezone` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /users/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

