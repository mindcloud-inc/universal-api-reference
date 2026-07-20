# Beamer: Update Post

Updates an existing post in Beamer.

```
PUT https://connect.mindcloud.co/v1/universal/beamer/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postId": 1,
  "title[]": [
    "string"
  ],
  "content[]": [
    "string"
  ],
  "category": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beamer/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postId": 1,
    "title[]": ["string"],
    "content[]": ["string"],
    "category": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postId` | number | yes |  |
| `title[]` | array<string> | yes | Accepts multiple values as an array. |
| `content[]` | array<string> | yes | Accepts multiple values as an array. |
| `category` | string | yes |  |
| `publish` | boolean | no |  |
| `archive` | boolean | no |  |
| `pinned` | boolean | no |  |
| `showInWidget` | boolean | no |  |
| `showInStandalone` | boolean | no |  |
| `boostedAnnouncement` | string | no |  |
| `linkUrl[]` | array<string> | no | Accepts multiple values as an array. |
| `linkText[]` | array<string> | no | Accepts multiple values as an array. |
| `linksInNewWindow` | boolean | no |  |
| `date` | string | no |  |
| `dueDate` | string | no |  |
| `language[]` | array<string> | no | Accepts multiple values as an array. |
| `filter` | string | no |  |
| `filterUserId` | string | no |  |
| `filterUrl` | string | no |  |
| `enableFeedback` | boolean | no |  |
| `enableReactions` | boolean | no |  |
| `enableSocialShare` | boolean | no |  |
| `autoOpen` | boolean | no |  |
| `sendPushNotification` | boolean | no |  |
| `userEmail` | string | no |  |
| `fixedBoostedAnnouncement` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `PUT /v0/posts/:postId` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

