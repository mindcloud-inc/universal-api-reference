# Scoro: View Permission Set

Retrieves permission set details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-permission-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-permission-set?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-permission-set?${params}`, {
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
| `id` | string | no | Scoro permission set ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "role_id": 1,
      "role_name": "Ava Chen",
      "role_users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `role_id` | number |  |
| `role_name` | string |  |
| `role_users` | array<object> |  |

## Native endpoint

Through the native Scoro API, this operation is `POST userRoles/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-permission-set.md) for the provider-specific parameters and requirements.

