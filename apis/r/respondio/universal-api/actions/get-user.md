# respond.io: Get User

Retrieves a user from respond.io.

```
GET https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-user?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "restrictions": {},
      "role": "string",
      "team": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | User email |
| `firstName` | string | User first name |
| `id` | number | User ID |
| `lastName` | string | User last name |
| `restrictions` | object | Workspace restriction details |
| `role` | string | Workspace role |
| `team` | object | Assigned team information |

## Native endpoint

Through the native respond.io API, this operation is `GET /space/user/:id` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

