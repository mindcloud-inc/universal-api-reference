# Dash.app: Get User

Retrieves a user from Dash.app by ID.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-user?connectionId=$CONNECTION_ID&id=google-oauth2%7C123%20or%20user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "google-oauth2|123 or user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The unique ID of the user or the user's email. Example: `google-oauth2\|123 or user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "name": "Ava Chen",
      "permissions": {},
      "picture": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastLogin` | date |  |
| `lastName` | string |  |
| `name` | string |  |
| `permissions` | object |  |
| `picture` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dash.app API, this operation is `GET /users/:id` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

