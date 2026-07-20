# Ship&Co: Register Sub User



```
POST https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-sub-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-sub-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-sub-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Sub-user email address. |
| `contact` | object | no | Sub-user contact object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `api_token` | boolean | no | Whether Ship&Co should generate an API token for the sub-user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Sub user company. |
| `created_at` | date | Sub user creation timestamp. |
| `email` | string | Sub user email address. |
| `first_name` | string | Sub user first name. |
| `id` | string | Created sub user ID. |
| `last_name` | string | Sub user last name. |
| `token` | string | Generated sub user API token when api_token is true. |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /sub-users` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-sub-user.md) for the provider-specific parameters and requirements.

