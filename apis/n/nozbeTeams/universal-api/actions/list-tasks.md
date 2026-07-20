# Nozbe Teams: List Tasks

Retrieves accessible tasks from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-tasks?${params}`, {
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
| `projectId` | string | no | Return only tasks from this project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": 1,
      "extra": "string",
      "id": "string",
      "isAbandoned": true,
      "isAllDay": true,
      "isFollowed": true,
      "lastActivityAt": 1,
      "lastModified": 1,
      "missedRepeats": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "projectPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | number |  |
| `extra` | string |  |
| `id` | string |  |
| `isAbandoned` | boolean |  |
| `isAllDay` | boolean |  |
| `isFollowed` | boolean |  |
| `lastActivityAt` | number |  |
| `lastModified` | number |  |
| `missedRepeats` | number |  |
| `name` | string |  |
| `projectId` | string |  |
| `projectPosition` | number |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `GET /tasks` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

