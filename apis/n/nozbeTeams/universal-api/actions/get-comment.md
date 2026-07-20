# Nozbe Teams: Get Comment

Retrieves a comment from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-comment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-comment?${params}`, {
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
| `id` | string | yes | The comment to retrieve. |

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

Through the native Nozbe Teams API, this operation is `GET /comments/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

