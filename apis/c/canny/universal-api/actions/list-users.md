# Canny: List Users

Retrieves all available users from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-users?${params}`, {
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
| `limit` | number | no |  |
| `cursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "avatarURL": "https://example.com",
      "companies": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "email": "ava@example.com",
      "id": "string",
      "isAdmin": true,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "url": "https://example.com",
      "userID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `avatarURL` | string |  |
| `companies` | array<object> |  |
| `created` | date |  |
| `customFields` | object |  |
| `email` | string |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `lastActivity` | date |  |
| `name` | string |  |
| `url` | string |  |
| `userID` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v2/users/list` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

