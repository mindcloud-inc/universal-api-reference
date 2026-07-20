# Tailwind: Schedule Post

Schedules an existing post in Tailwind.

```
PUT https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/schedule-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/schedule-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "postId": "string",
  "sendAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/schedule-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "postId": "string",
    "sendAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Pinterest account ID. |
| `postId` | string | yes | Tailwind post ID. |
| `sendAt` | date | yes | ISO 8601 time when the post should be published. |
| `boardId` | string | no | Target board ID. Required when scheduling a draft that does not already have a board. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "boardId": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "isSimplifiedPin": true,
      "mediaType": "string",
      "mediaUrl": "https://example.com",
      "pinId": "string",
      "sendAt": 1,
      "sentAt": 1,
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string | Alt text. |
| `boardId` | string | Board ID. |
| `createdAt` | number | Creation time as a Unix timestamp. |
| `description` | string | Pin description. |
| `id` | string | Post ID. |
| `isSimplifiedPin` | boolean | Whether the post is a simplified pin. |
| `mediaType` | string | Media type. |
| `mediaUrl` | string | Media file URL. |
| `pinId` | string | Pinterest pin ID after publishing. |
| `sendAt` | number | Scheduled send time as a Unix timestamp. |
| `sentAt` | number | Actual send time as a Unix timestamp. |
| `status` | string | Post status. |
| `title` | string | Pin title. |
| `url` | string | Destination URL. |

## Native endpoint

Through the native Tailwind API, this operation is `POST /v1/accounts/:accountId/posts/:postId/schedule` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-post.md) for the provider-specific parameters and requirements.

