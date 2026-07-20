# Podio: Add Comment to Object

Creates a comment on a Podio object.

```
POST https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-comment-to-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-comment-to-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "item",
  "id": "12345",
  "value": "Please review the updated timeline."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-comment-to-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "item",
    "id": "12345",
    "value": "Please review the updated timeline."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | The type of object to comment on. Example: `item`. |
| `id` | string | yes | The ID of the object to comment on. Example: `12345`. |
| `value` | string | yes | The comment text to add. Example: `Please review the updated timeline.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | An external ID for the comment, if any. Example: `comment-123`. |
| `fileIds[]` | array<string> | no | Uploaded file IDs to attach to the comment. |
| `embedId` | string | no | The ID of an embedded link created in Podio. Example: `12345`. |
| `embedUrl` | string | no | A URL to attach to the comment. Example: `https://example.com/spec`. |
| `alertInvite` | boolean | no | Automatically invite mentioned users when needed. |
| `hook` | boolean | no | Run Podio hooks for the change. |
| `silent` | boolean | no | Suppress stream bumping and notifications for the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": 1,
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "embed": {},
      "embedFile": {},
      "externalId": "string",
      "files": [
        {}
      ],
      "grantedUsers": [
        {}
      ],
      "invitedUsers": [
        {}
      ],
      "isLiked": true,
      "lastEditOn": "2026-05-07T12:00:00.000Z",
      "likeCount": 1,
      "questions": [
        {}
      ],
      "ref": {},
      "richValue": "string",
      "rights": [
        "string"
      ],
      "user": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | number |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `embed` | object |  |
| `embedFile` | object |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `grantedUsers` | array<object> |  |
| `invitedUsers` | array<object> |  |
| `isLiked` | boolean |  |
| `lastEditOn` | date |  |
| `likeCount` | number |  |
| `questions` | array<object> |  |
| `ref` | object |  |
| `richValue` | string |  |
| `rights` | array<string> |  |
| `user` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Podio API, this operation is `POST /comment/:type/:id/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-to-object.md) for the provider-specific parameters and requirements.

