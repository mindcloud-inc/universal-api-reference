# Incontrol: Get User

Retrieves details for a user from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerified": true,
      "firstname": "Ava",
      "groups": [
        {}
      ],
      "id": "string",
      "language": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "lastname": "Chen",
      "organization": {},
      "rights": [
        "string"
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `email` | string | User email address. |
| `emailVerified` | boolean | Whether the user's email is verified. |
| `firstname` | string | User first name. |
| `groups` | array<object> | Groups associated with the user. |
| `id` | string | User ID. |
| `language` | string | User language code. |
| `lastActivity` | date | Last recorded user activity timestamp. |
| `lastname` | string | User last name. |
| `organization` | object | Organization summary for the user. |
| `rights` | array<string> | Rights associated with the user. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/user/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

