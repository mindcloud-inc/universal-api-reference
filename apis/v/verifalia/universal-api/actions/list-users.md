# Verifalia: List Users

Retrieves users from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-users?${params}`, {
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
| `sort` | string | no | Sort users by `createdOn`, `-createdOn`, `displayName`, or `-displayName`. |
| `type` | string | no | Filter users by Verifalia type: `Administrator`, `Standard`, or `BrowserApp`. |
| `includeDeleted` | boolean | no | Set to true to include deleted users in the listing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "id": "string",
      "isActive": true,
      "isDeleted": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | The user's display name. |
| `id` | string | The Verifalia user ID. |
| `isActive` | boolean | Whether the user is active. |
| `isDeleted` | boolean | Whether the user has been deleted. |
| `type` | string | The Verifalia user type. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /users` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

