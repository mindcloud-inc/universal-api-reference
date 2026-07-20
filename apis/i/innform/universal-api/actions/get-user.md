# Innform: Get User

Retrieves a user from Innform by ID or email.

```
GET https://connect.mindcloud.co/v1/universal/innform/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/get-user?connectionId=$CONNECTION_ID&idOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/get-user?${params}`, {
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
| `idOrEmail` | string | yes | User UUID or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignments": [
        {}
      ],
      "email": "ava@example.com",
      "groups": [
        {}
      ],
      "id": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "property": {},
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignments` | array<object> |  |
| `email` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `property` | object |  |
| `role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Innform API, this operation is `GET /users/{idOrEmail}` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

