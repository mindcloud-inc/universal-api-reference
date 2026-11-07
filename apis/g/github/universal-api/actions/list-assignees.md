# GitHub: List Assignees

Retrieves the users who can be assigned to issues in a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-assignees?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-assignees?${params}`, {
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
| `owner` | string | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | string | yes | The name of the repository without the .git extension. The name is not case sensitive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "login": "Ava Chen",
      "htmlUrl": "https://example.com",
      "type": "string",
      "id": 1,
      "siteAdmin": true,
      "avatarUrl": "https://example.com",
      "eventsUrl": "https://example.com",
      "followersUrl": "https://example.com",
      "followingUrl": "https://example.com",
      "gistsUrl": "https://example.com",
      "gravatarId": "string",
      "nodeId": "string",
      "organizationsUrl": "https://example.com",
      "receivedEventsUrl": "https://example.com",
      "reposUrl": "https://example.com",
      "starredUrl": "https://example.com",
      "subscriptionsUrl": "https://example.com",
      "url": "https://example.com",
      "userViewType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `login` | string |  |
| `htmlUrl` | string |  |
| `type` | string |  |
| `id` | number |  |
| `siteAdmin` | boolean |  |
| `avatarUrl` | string |  |
| `eventsUrl` | string |  |
| `followersUrl` | string |  |
| `followingUrl` | string |  |
| `gistsUrl` | string |  |
| `gravatarId` | string |  |
| `nodeId` | string |  |
| `organizationsUrl` | string |  |
| `receivedEventsUrl` | string |  |
| `reposUrl` | string |  |
| `starredUrl` | string |  |
| `subscriptionsUrl` | string |  |
| `url` | string |  |
| `userViewType` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/assignees` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assignees.md) for the provider-specific parameters and requirements.

