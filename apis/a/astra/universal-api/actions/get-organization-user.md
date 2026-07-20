# Astra: Get Organization User

Retrieves one organization user from Astra.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-organization-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-organization-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-organization-user?${params}`, {
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
| `userId` | string | yes | The Astra organization user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Email": "ava@example.com",
      "Roles": [
        {}
      ],
      "Status": "string",
      "UserID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string | The user email address. |
| `Roles` | array<object> | Roles assigned to the user. |
| `Status` | string | The user status. |
| `UserID` | string | The Astra user ID. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/organizations/users/:userId` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-user.md) for the provider-specific parameters and requirements.

