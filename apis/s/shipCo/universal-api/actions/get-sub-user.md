# Ship&Co: Get Sub User



```
GET https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-sub-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-sub-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-sub-user?${params}`, {
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
| `id` | string | yes | Ship&Co sub-user ID. Ship&Co requires a 32-character sub-user ID. |

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
| `id` | string | Sub user ID. |
| `last_name` | string | Sub user last name. |
| `token` | string | Sub user API token when returned by Ship&Co. |

## Native endpoint

Through the native Ship&Co API, this operation is `GET /sub-users/:id` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sub-user.md) for the provider-specific parameters and requirements.

