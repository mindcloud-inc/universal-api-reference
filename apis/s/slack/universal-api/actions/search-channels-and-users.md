# Slack: Search Channels and Users

Finds Slack channels and users by search query.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-channels-and-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-channels-and-users?connectionId=$CONNECTION_ID&limit=25&offset=0&query=project%20gizmo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "project gizmo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-channels-and-users?${params}`, {
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
| `query` | string | yes | User prompt or search query Example: `project gizmo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "permalink": "https://example.com",
      "profilePicPermalink": "https://example.com",
      "timezone": "string",
      "title": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullName` | string |  |
| `permalink` | string |  |
| `profilePicPermalink` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST assistant.search.context` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-channels-and-users.md) for the provider-specific parameters and requirements.

