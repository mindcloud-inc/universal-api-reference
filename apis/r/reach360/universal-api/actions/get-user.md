# Reach360: Get User

Retrieves a user from Reach360 by ID.

```
GET https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articulate360User": true,
      "email": "ava@example.com",
      "favoritesUrl": "https://example.com",
      "firstName": "Ava",
      "groupsUrl": "https://example.com",
      "id": "string",
      "lastActiveAt": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "learnerReportUrl": "https://example.com",
      "managingGroupsUrl": "https://example.com",
      "reportingGroupsUrl": "https://example.com",
      "role": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articulate360User` | boolean |  |
| `email` | string |  |
| `favoritesUrl` | string |  |
| `firstName` | string |  |
| `groupsUrl` | string |  |
| `id` | string |  |
| `lastActiveAt` | date |  |
| `lastName` | string |  |
| `learnerReportUrl` | string |  |
| `managingGroupsUrl` | string |  |
| `reportingGroupsUrl` | string |  |
| `role` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Reach360 API, this operation is `GET /users/:userId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

