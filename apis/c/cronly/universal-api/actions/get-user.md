# Cronly: Get User



```
GET https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | The ID of the user to view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "is_super_admin": true,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | number |  |
| `is_super_admin` | boolean |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Cronly API, this operation is `GET /api/users/:id` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

