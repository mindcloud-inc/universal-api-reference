# MoreApp: Retrieve User

Retrieves a user from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&customerId=209321&userId=69bc2775994b3bfa30c02bef" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "userId": "69bc2775994b3bfa30c02bef"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-user?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `userId` | string | yes | MoreApp user identifier. Default: `69bc2775994b3bfa30c02bef`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "emailAddress": "ava@example.com",
      "emailValidated": true,
      "externallyManaged": true,
      "grants": [
        {}
      ],
      "groups": [
        {}
      ],
      "id": "string",
      "settings": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean |  |
| `emailAddress` | string |  |
| `emailValidated` | boolean |  |
| `externallyManaged` | boolean |  |
| `grants` | array<object> |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `settings` | object |  |
| `username` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/customers/{{customerId}}/users/{{userId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

