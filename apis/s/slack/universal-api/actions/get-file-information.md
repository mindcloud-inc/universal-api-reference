# Slack: Get File Information

Retrieves file details from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-information?connectionId=$CONNECTION_ID&limit=25&offset=0&channel=string&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channel": "string",
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-information?${params}`, {
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
| `channel` | list | yes | Channel containing the file. |
| `file` | list | yes | ID of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {
        "channels": [
          "string"
        ],
        "commentsCount": 1,
        "created": 1,
        "displayAsBot": true,
        "editable": true,
        "externalType": "string",
        "fileAccess": "string",
        "filetype": "string",
        "hasMoreShares": true,
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
        "shares": {
          "public": {
            "c3mavjkv0": [
              {
                "channelName": "Ava Chen",
                "isSilentShare": true,
                "latestReply": "string",
                "replyCount": 1,
                "replyUsers": [
                  "string"
                ],
                "replyUsersCount": 1,
                "shareUserId": "string",
                "source": "string",
                "teamId": "string",
                "ts": "string"
              }
            ]
          }
        },
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file.channels[]` | string |  |
| `file.commentsCount` | number |  |
| `file.created` | number |  |
| `file.displayAsBot` | boolean |  |
| `file.editable` | boolean |  |
| `file.externalType` | string |  |
| `file.fileAccess` | string |  |
| `file.filetype` | string |  |
| `file.hasMoreShares` | boolean |  |
| `file.hasRichPreview` | boolean |  |
| `file.id` | string |  |
| `file.isExternal` | boolean |  |
| `file.isPublic` | boolean |  |
| `file.isStarred` | boolean |  |
| `file.mediaDisplayType` | string |  |
| `file.mimetype` | string |  |
| `file.mode` | string |  |
| `file.name` | string |  |
| `file.originalH` | number |  |
| `file.originalW` | number |  |
| `file.permalink` | string |  |
| `file.permalinkPublic` | string |  |
| `file.prettyType` | string |  |
| `file.publicUrlShared` | boolean |  |
| `file.shares.public.c3mavjkv0[].channelName` | string |  |
| `file.shares.public.c3mavjkv0[].isSilentShare` | boolean |  |
| `file.shares.public.c3mavjkv0[].latestReply` | string |  |
| `file.shares.public.c3mavjkv0[].replyCount` | number |  |
| `file.shares.public.c3mavjkv0[].replyUsers[]` | string |  |
| `file.shares.public.c3mavjkv0[].replyUsersCount` | number |  |
| `file.shares.public.c3mavjkv0[].shareUserId` | string |  |
| `file.shares.public.c3mavjkv0[].source` | string |  |
| `file.shares.public.c3mavjkv0[].teamId` | string |  |
| `file.shares.public.c3mavjkv0[].ts` | string |  |
| `file.size` | number |  |
| `file.thumb1024` | string |  |
| `file.thumb1024H` | number |  |
| `file.thumb1024W` | number |  |
| `file.thumb160` | string |  |
| `file.thumb360` | string |  |
| `file.thumb360H` | number |  |
| `file.thumb360W` | number |  |
| `file.thumb480` | string |  |
| `file.thumb480H` | number |  |
| `file.thumb480W` | number |  |
| `file.thumb64` | string |  |
| `file.thumb720` | string |  |
| `file.thumb720H` | number |  |
| `file.thumb720W` | number |  |
| `file.thumb80` | string |  |
| `file.thumb800` | string |  |
| `file.thumb800H` | number |  |
| `file.thumb800W` | number |  |
| `file.thumb960` | string |  |
| `file.thumb960H` | number |  |
| `file.thumb960W` | number |  |
| `file.thumbTiny` | string |  |
| `file.timestamp` | number |  |
| `file.title` | string |  |
| `file.urlPrivate` | string |  |
| `file.urlPrivateDownload` | string |  |
| `file.user` | string |  |
| `file.username` | string |  |
| `file.userTeam` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET files.info` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-file-information.md) for the provider-specific parameters and requirements.

