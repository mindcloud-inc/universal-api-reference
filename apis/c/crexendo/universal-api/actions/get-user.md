# Crexendo: Get User

Retrieves a user from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-user?connectionId=$CONNECTION_ID&domain=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-user?${params}`, {
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
| `domain` | string | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | string | yes | User extension or identifier, for example 1000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account-status": "string",
      "created-datetime": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "email": "ava@example.com",
      "login-username": "Ava Chen",
      "name-first-name": "Ava Chen",
      "name-last-name": "Ava Chen",
      "user": "string",
      "user-scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account-status` | string |  |
| `created-datetime` | date |  |
| `domain` | string |  |
| `email` | string |  |
| `login-username` | string |  |
| `name-first-name` | string |  |
| `name-last-name` | string |  |
| `user` | string |  |
| `user-scope` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/:domain/users/:user` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

