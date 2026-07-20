# Zoho Connect: Get Single Feed

Retrieves a single feed from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-single-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-single-feed?connectionId=$CONNECTION_ID&scopeId=string&streamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string",
  "streamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-single-feed?${params}`, {
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
| `scopeId` | string | yes | ID of the network where the post was made. |
| `streamId` | string | yes | The post to fetch by ID. |
| `streamUrl` | string | no | Optional post URL to fetch the post instead of the ID. |
| `commentIndex` | number | no | Start index for comments. The default is 0. |
| `commentLimit` | number | no | Set a limit on the number of comments. The default is 20. |
| `isThread` | boolean | no | Set to true for threaded comments, or false for normal view. |
| `needAllComments` | boolean | no | Set to true to return all comments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "singleStream": {
        "stream": {
          "allowFooter": true,
          "answers": [
            {}
          ],
          "canAddTask": true,
          "canDelete": true,
          "canEdit": true,
          "canFollow": true,
          "canLock": true,
          "canMarkAsReadLater": true,
          "canMove": true,
          "canShare": true,
          "canShowPostAudit": true,
          "canShowPostInsight": true,
          "canTranslate": true,
          "commentCount": 1,
          "comments": [
            {}
          ],
          "commentViewType": "string",
          "content": "string",
          "formatedTime": "string",
          "id": "string",
          "isApproved": true,
          "lastRepliedTime": "string",
          "mentionedUsers": [
            {}
          ],
          "moduleName": "Ava Chen",
          "reason": {
            "msg": "string"
          },
          "status": "string",
          "streamModifiedTime": "string",
          "streamParticipants": [
            {}
          ],
          "time": "string",
          "title": "string",
          "type": "string",
          "uniqueViewCount": 1,
          "url": "https://example.com",
          "userDetails": {
            "canFollow": true,
            "id": "string",
            "imageUrl": "https://example.com",
            "name": "Ava Chen",
            "type": "string",
            "zuid": "string"
          },
          "userIds": [
            "string"
          ],
          "viewCount": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `singleStream.stream.allowFooter` | boolean |  |
| `singleStream.stream.answers` | array<object> |  |
| `singleStream.stream.canAddTask` | boolean |  |
| `singleStream.stream.canDelete` | boolean |  |
| `singleStream.stream.canEdit` | boolean |  |
| `singleStream.stream.canFollow` | boolean |  |
| `singleStream.stream.canLock` | boolean |  |
| `singleStream.stream.canMarkAsReadLater` | boolean |  |
| `singleStream.stream.canMove` | boolean |  |
| `singleStream.stream.canShare` | boolean |  |
| `singleStream.stream.canShowPostAudit` | boolean |  |
| `singleStream.stream.canShowPostInsight` | boolean |  |
| `singleStream.stream.canTranslate` | boolean |  |
| `singleStream.stream.commentCount` | number |  |
| `singleStream.stream.comments` | array<object> |  |
| `singleStream.stream.commentViewType` | string |  |
| `singleStream.stream.content` | string |  |
| `singleStream.stream.formatedTime` | string |  |
| `singleStream.stream.id` | string |  |
| `singleStream.stream.isApproved` | boolean |  |
| `singleStream.stream.lastRepliedTime` | string |  |
| `singleStream.stream.mentionedUsers` | array<object> |  |
| `singleStream.stream.moduleName` | string |  |
| `singleStream.stream.reason.msg` | string |  |
| `singleStream.stream.status` | string |  |
| `singleStream.stream.streamModifiedTime` | string |  |
| `singleStream.stream.streamParticipants` | array<object> |  |
| `singleStream.stream.time` | string |  |
| `singleStream.stream.title` | string |  |
| `singleStream.stream.type` | string |  |
| `singleStream.stream.uniqueViewCount` | number |  |
| `singleStream.stream.url` | string |  |
| `singleStream.stream.userDetails.canFollow` | boolean |  |
| `singleStream.stream.userDetails.id` | string |  |
| `singleStream.stream.userDetails.imageUrl` | string |  |
| `singleStream.stream.userDetails.name` | string |  |
| `singleStream.stream.userDetails.type` | string |  |
| `singleStream.stream.userDetails.zuid` | string |  |
| `singleStream.stream.userIds` | array<string> |  |
| `singleStream.stream.viewCount` | number |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/v1/singleStream` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-feed.md) for the provider-specific parameters and requirements.

