# Zoho Connect: Start a Feed

Creates a new feed in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/start-a-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/start-a-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/start-a-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes | ID of the network where the post should be shared. |
| `partitionId` | string | no | Optional group or company wall partition ID. |
| `streamContent` | string | yes | Content for the post. Maximum length is 10000 characters and it supports mentions plus rich formatting. |
| `streamTitle` | string | no | Optional title for the post. |
| `linkUrl` | string | no | Optional link to attach to the post. |
| `linkDesc` | string | no | Optional description for the attached link. |
| `linkTitle` | string | no | Optional title for the attached link. |
| `linkImage` | string | no | Optional image URL for the attached link. |
| `fileIds` | string | no | Comma-separated file IDs from the upload Files API. Up to 10 files can be attached. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addStream": {
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
| `addStream.stream.allowFooter` | boolean |  |
| `addStream.stream.answers` | array<object> |  |
| `addStream.stream.canAddTask` | boolean |  |
| `addStream.stream.canDelete` | boolean |  |
| `addStream.stream.canEdit` | boolean |  |
| `addStream.stream.canFollow` | boolean |  |
| `addStream.stream.canLock` | boolean |  |
| `addStream.stream.canMarkAsReadLater` | boolean |  |
| `addStream.stream.canMove` | boolean |  |
| `addStream.stream.canShare` | boolean |  |
| `addStream.stream.canShowPostAudit` | boolean |  |
| `addStream.stream.canShowPostInsight` | boolean |  |
| `addStream.stream.canTranslate` | boolean |  |
| `addStream.stream.commentCount` | number |  |
| `addStream.stream.comments` | array<object> |  |
| `addStream.stream.commentViewType` | string |  |
| `addStream.stream.content` | string |  |
| `addStream.stream.formatedTime` | string |  |
| `addStream.stream.id` | string |  |
| `addStream.stream.isApproved` | boolean |  |
| `addStream.stream.lastRepliedTime` | string |  |
| `addStream.stream.mentionedUsers` | array<object> |  |
| `addStream.stream.moduleName` | string |  |
| `addStream.stream.reason.msg` | string |  |
| `addStream.stream.status` | string |  |
| `addStream.stream.streamModifiedTime` | string |  |
| `addStream.stream.streamParticipants` | array<object> |  |
| `addStream.stream.time` | string |  |
| `addStream.stream.title` | string |  |
| `addStream.stream.type` | string |  |
| `addStream.stream.uniqueViewCount` | number |  |
| `addStream.stream.url` | string |  |
| `addStream.stream.userDetails.canFollow` | boolean |  |
| `addStream.stream.userDetails.id` | string |  |
| `addStream.stream.userDetails.imageUrl` | string |  |
| `addStream.stream.userDetails.name` | string |  |
| `addStream.stream.userDetails.type` | string |  |
| `addStream.stream.userDetails.zuid` | string |  |
| `addStream.stream.userIds` | array<string> |  |
| `addStream.stream.viewCount` | number |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/v2/addStream` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-a-feed.md) for the provider-specific parameters and requirements.

