# Slack: List User Reactions

Retrieves reactions made by a Slack user.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-user-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-user-reactions?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-user-reactions?${params}`, {
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
| `user` | list | yes | Show reactions made by this user. Defaults to the authed user. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `full` | boolean | no | If true always return the complete reaction list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "message": {
        "clientMsgId": "string",
        "displayAsBot": true,
        "files": [
          {
            "created": 1,
            "displayAsBot": true,
            "editable": true,
            "externalType": "string",
            "fileAccess": "string",
            "filetype": "string",
            "hasRichPreview": true,
            "id": "string",
            "isExternal": true,
            "isPublic": true,
            "isStarred": true,
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
            "skippedShares": true,
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
        "isLocked": true,
        "lastRead": "string",
        "latestReply": "string",
        "permalink": "https://example.com",
        "reactions": [
          {
            "count": 1,
            "name": "Ava Chen",
            "users": [
              "string"
            ]
          }
        ],
        "replyCount": 1,
        "replyUsers": [
          "string"
        ],
        "replyUsersCount": 1,
        "subscribed": true,
        "text": "string",
        "threadTs": "string",
        "ts": "string",
        "type": "string",
        "upload": true,
        "user": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `message.clientMsgId` | string |  |
| `message.displayAsBot` | boolean |  |
| `message.files[].created` | number |  |
| `message.files[].displayAsBot` | boolean |  |
| `message.files[].editable` | boolean |  |
| `message.files[].externalType` | string |  |
| `message.files[].fileAccess` | string |  |
| `message.files[].filetype` | string |  |
| `message.files[].hasRichPreview` | boolean |  |
| `message.files[].id` | string |  |
| `message.files[].isExternal` | boolean |  |
| `message.files[].isPublic` | boolean |  |
| `message.files[].isStarred` | boolean |  |
| `message.files[].mediaDisplayType` | string |  |
| `message.files[].mimetype` | string |  |
| `message.files[].mode` | string |  |
| `message.files[].name` | string |  |
| `message.files[].originalH` | number |  |
| `message.files[].originalW` | number |  |
| `message.files[].permalink` | string |  |
| `message.files[].permalinkPublic` | string |  |
| `message.files[].prettyType` | string |  |
| `message.files[].publicUrlShared` | boolean |  |
| `message.files[].size` | number |  |
| `message.files[].skippedShares` | boolean |  |
| `message.files[].thumb1024` | string |  |
| `message.files[].thumb1024H` | number |  |
| `message.files[].thumb1024W` | number |  |
| `message.files[].thumb160` | string |  |
| `message.files[].thumb360` | string |  |
| `message.files[].thumb360H` | number |  |
| `message.files[].thumb360W` | number |  |
| `message.files[].thumb480` | string |  |
| `message.files[].thumb480H` | number |  |
| `message.files[].thumb480W` | number |  |
| `message.files[].thumb64` | string |  |
| `message.files[].thumb720` | string |  |
| `message.files[].thumb720H` | number |  |
| `message.files[].thumb720W` | number |  |
| `message.files[].thumb80` | string |  |
| `message.files[].thumb800` | string |  |
| `message.files[].thumb800H` | number |  |
| `message.files[].thumb800W` | number |  |
| `message.files[].thumb960` | string |  |
| `message.files[].thumb960H` | number |  |
| `message.files[].thumb960W` | number |  |
| `message.files[].thumbTiny` | string |  |
| `message.files[].timestamp` | number |  |
| `message.files[].title` | string |  |
| `message.files[].urlPrivate` | string |  |
| `message.files[].urlPrivateDownload` | string |  |
| `message.files[].user` | string |  |
| `message.files[].username` | string |  |
| `message.files[].userTeam` | string |  |
| `message.isLocked` | boolean |  |
| `message.lastRead` | string |  |
| `message.latestReply` | string |  |
| `message.permalink` | string |  |
| `message.reactions[].count` | number |  |
| `message.reactions[].name` | string |  |
| `message.reactions[].users[]` | string |  |
| `message.replyCount` | number |  |
| `message.replyUsers[]` | string |  |
| `message.replyUsersCount` | number |  |
| `message.subscribed` | boolean |  |
| `message.text` | string |  |
| `message.threadTs` | string |  |
| `message.ts` | string |  |
| `message.type` | string |  |
| `message.upload` | boolean |  |
| `message.user` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET reactions.list` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-reactions.md) for the provider-specific parameters and requirements.

