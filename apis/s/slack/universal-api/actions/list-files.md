# Slack: List Files

Retrieves files from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0&channel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-files?${params}`, {
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
| `channel` | list<string> | yes | Filter files appearing in a specific channel, indicated by its ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showFilesHiddenByLimit` | boolean | no | Show truncated file info for files hidden due to being too old, and the team who owns the file being over the file limit |
| `tsFrom` | date | no | Filter files created after this timestamp (inclusive). |
| `tsTo` | date | no | Filter files created before this timestamp (inclusive). |
| `types` | list<string> | no | Filter files by type Accepts multiple values as an array. |
| `user` | list<string> | no | Filter files created by a single user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        "string"
      ],
      "commentsCount": 1,
      "created": 1,
      "displayAsBot": true,
      "editable": true,
      "externalType": "string",
      "filetype": "string",
      "id": "string",
      "isExternal": true,
      "isPublic": true,
      "mediaDisplayType": "string",
      "mimetype": "string",
      "mode": "string",
      "name": "Ava Chen",
      "originalH": 1,
      "originalW": 1,
      "permalink": "https://example.com",
      "permalinkPublic": "https://example.com",
      "prettyType": "string",
      "publicUrlShared": true,
      "size": 1,
      "thumb1024": "string",
      "thumb1024H": 1,
      "thumb1024W": 1,
      "thumb160": "string",
      "thumb360": "string",
      "thumb360H": 1,
      "thumb360W": 1,
      "thumb480": "string",
      "thumb480H": 1,
      "thumb480W": 1,
      "thumb64": "string",
      "thumb720": "string",
      "thumb720H": 1,
      "thumb720W": 1,
      "thumb80": "string",
      "thumb800": "string",
      "thumb800H": 1,
      "thumb800W": 1,
      "thumb960": "string",
      "thumb960H": 1,
      "thumb960W": 1,
      "thumbTiny": "string",
      "timestamp": 1,
      "title": "string",
      "urlPrivate": "https://example.com",
      "urlPrivateDownload": "https://example.com",
      "user": "string",
      "username": "Ava Chen",
      "userTeam": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[]` | string |  |
| `commentsCount` | number |  |
| `created` | number |  |
| `displayAsBot` | boolean |  |
| `editable` | boolean |  |
| `externalType` | string |  |
| `filetype` | string |  |
| `id` | string |  |
| `isExternal` | boolean |  |
| `isPublic` | boolean |  |
| `mediaDisplayType` | string |  |
| `mimetype` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `originalH` | number |  |
| `originalW` | number |  |
| `permalink` | string |  |
| `permalinkPublic` | string |  |
| `prettyType` | string |  |
| `publicUrlShared` | boolean |  |
| `size` | number |  |
| `thumb1024` | string |  |
| `thumb1024H` | number |  |
| `thumb1024W` | number |  |
| `thumb160` | string |  |
| `thumb360` | string |  |
| `thumb360H` | number |  |
| `thumb360W` | number |  |
| `thumb480` | string |  |
| `thumb480H` | number |  |
| `thumb480W` | number |  |
| `thumb64` | string |  |
| `thumb720` | string |  |
| `thumb720H` | number |  |
| `thumb720W` | number |  |
| `thumb80` | string |  |
| `thumb800` | string |  |
| `thumb800H` | number |  |
| `thumb800W` | number |  |
| `thumb960` | string |  |
| `thumb960H` | number |  |
| `thumb960W` | number |  |
| `thumbTiny` | string |  |
| `timestamp` | number |  |
| `title` | string |  |
| `urlPrivate` | string |  |
| `urlPrivateDownload` | string |  |
| `user` | string |  |
| `username` | string |  |
| `userTeam` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET files.list` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

