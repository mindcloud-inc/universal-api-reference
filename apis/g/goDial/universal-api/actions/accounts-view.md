# GoDial: Get User

Retrieves details for a user from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-view?${params}`, {
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
| `id` | string | yes | Account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "forcePasswordReset": true,
      "id": "string",
      "isEmailVerified": true,
      "lists": [
        {}
      ],
      "name": "Ava Chen",
      "permissions": {},
      "phone": "string",
      "role": "string",
      "teams": [
        {}
      ],
      "teamsId": [
        "string"
      ],
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdOn` | date |  |
| `email` | string |  |
| `forcePasswordReset` | boolean |  |
| `id` | string |  |
| `isEmailVerified` | boolean |  |
| `lists` | array<object> |  |
| `name` | string |  |
| `permissions` | object |  |
| `phone` | string |  |
| `role` | string |  |
| `teams` | array<object> |  |
| `teamsId` | array<string> |  |
| `username` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/accounts/[:id]/view` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accounts-view.md) for the provider-specific parameters and requirements.

