# Nozbe Teams: List Comments

Retrieves accessible comments from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-comments?${params}`, {
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
| `taskId` | string | no | Return only comments for this task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "body": "string",
      "createdAt": 1,
      "extra": "string",
      "id": "string",
      "isDeleted": true,
      "isPinned": true,
      "isTeam": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `body` | string |  |
| `createdAt` | number |  |
| `extra` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isPinned` | boolean |  |
| `isTeam` | boolean |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `GET /comments` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

