# Klipfolio: List Group Users

Retrieves users assigned to a Klipfolio group.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-group-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-group-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-group-users?${params}`, {
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
| `groupId` | string | no | The Klipfolio group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "date_created": "string",
      "date_last_login": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "is_locked_out": true,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `date_created` | string |  |
| `date_last_login` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `is_locked_out` | boolean |  |
| `last_name` | string |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /groups/:groupId/users` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-users.md) for the provider-specific parameters and requirements.

