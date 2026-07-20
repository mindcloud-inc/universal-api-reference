# Vero: Delete User

Deletes an existing user from Vero.

```
DELETE https://connect.mindcloud.co/v1/universal/vero/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vero/latest/actions/delete-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/delete-user?${params}`, {
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
| `id` | string | yes | The unique identifier of the user to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable Vero result message. |
| `status` | number | HTTP-style status code returned by Vero. |

## Native endpoint

Through the native Vero API, this operation is `POST /api/v2/users/delete` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

