# Slack: List Channel Messages

Retrieves channel messages and events from Slack.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&channel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channel-messages?${params}`, {
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
| `channel` | list | yes | Conversation ID to fetch history for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeAllMetadata` | boolean | no | Return all metadata associated with this message. |
| `inclusive` | boolean | no | Include messages with oldest or latest timestamps in results. Ignored unless either timestamp is specified. |
| `latest` | date | no | Only messages before this Unix timestamp will be included in results. |
| `oldest` | date | no | Only messages after this Unix timestamp will be included in results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocks": [
        {
          "blockId": "string",
          "elements": [
            {
              "elements": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        }
      ],
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
      "inviter": "string",
      "isLocked": true,
      "lastRead": "string",
      "latestReply": "string",
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
      "subtype": "string",
      "team": "string",
      "text": "string",
      "threadTs": "string",
      "ts": "string",
      "type": "string",
      "upload": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocks[].blockId` | string |  |
| `blocks[].elements[].elements[].text` | string |  |
| `blocks[].elements[].elements[].type` | string |  |
| `blocks[].elements[].type` | string |  |
| `blocks[].type` | string |  |
| `clientMsgId` | string |  |
| `displayAsBot` | boolean |  |
| `files[].created` | number |  |
| `files[].displayAsBot` | boolean |  |
| `files[].editable` | boolean |  |
| `files[].externalType` | string |  |
| `files[].fileAccess` | string |  |
| `files[].filetype` | string |  |
| `files[].hasRichPreview` | boolean |  |
| `files[].id` | string |  |
| `files[].isExternal` | boolean |  |
| `files[].isPublic` | boolean |  |
| `files[].isStarred` | boolean |  |
| `files[].mediaDisplayType` | string |  |
| `files[].mimetype` | string |  |
| `files[].mode` | string |  |
| `files[].name` | string |  |
| `files[].originalH` | number |  |
| `files[].originalW` | number |  |
| `files[].permalink` | string |  |
| `files[].permalinkPublic` | string |  |
| `files[].prettyType` | string |  |
| `files[].publicUrlShared` | boolean |  |
| `files[].size` | number |  |
| `files[].skippedShares` | boolean |  |
| `files[].thumb1024` | string |  |
| `files[].thumb1024H` | number |  |
| `files[].thumb1024W` | number |  |
| `files[].thumb160` | string |  |
| `files[].thumb360` | string |  |
| `files[].thumb360H` | number |  |
| `files[].thumb360W` | number |  |
| `files[].thumb480` | string |  |
| `files[].thumb480H` | number |  |
| `files[].thumb480W` | number |  |
| `files[].thumb64` | string |  |
| `files[].thumb720` | string |  |
| `files[].thumb720H` | number |  |
| `files[].thumb720W` | number |  |
| `files[].thumb80` | string |  |
| `files[].thumb800` | string |  |
| `files[].thumb800H` | number |  |
| `files[].thumb800W` | number |  |
| `files[].thumb960` | string |  |
| `files[].thumb960H` | number |  |
| `files[].thumb960W` | number |  |
| `files[].thumbTiny` | string |  |
| `files[].timestamp` | number |  |
| `files[].title` | string |  |
| `files[].urlPrivate` | string |  |
| `files[].urlPrivateDownload` | string |  |
| `files[].user` | string |  |
| `files[].username` | string |  |
| `files[].userTeam` | string |  |
| `inviter` | string |  |
| `isLocked` | boolean |  |
| `lastRead` | string |  |
| `latestReply` | string |  |
| `reactions[].count` | number |  |
| `reactions[].name` | string |  |
| `reactions[].users[]` | string |  |
| `replyCount` | number |  |
| `replyUsers[]` | string |  |
| `replyUsersCount` | number |  |
| `subscribed` | boolean |  |
| `subtype` | string |  |
| `team` | string |  |
| `text` | string |  |
| `threadTs` | string |  |
| `ts` | string |  |
| `type` | string |  |
| `upload` | boolean |  |
| `user` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST conversations.history` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-messages.md) for the provider-specific parameters and requirements.

