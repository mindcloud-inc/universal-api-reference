# Tailwind: Create Post

Creates a new post in Tailwind.

```
POST https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "mediaUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "mediaUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Pinterest account ID. |
| `mediaUrl` | string | yes | Publicly accessible image or video URL to pin. |
| `mediaType` | string | no | Media type. Defaults to image. One of: `0`, `1`. |
| `title` | string | no | Pin title. Required when scheduling via sendAt. |
| `description` | string | no | Pin description. Required when scheduling via sendAt. |
| `url` | string | no | Destination URL when the pin is clicked. Required when scheduling via sendAt. |
| `boardId` | string | no | Target board ID. Required when scheduling via sendAt. |
| `altText` | string | no | Alt text for accessibility. |
| `sendAt` | date | no | ISO 8601 time to schedule the post. If omitted, the post is saved as a draft. |
| `isSimplifiedPin` | boolean | no | Whether to create a simplified pin. Defaults to true. |

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

Through the native Tailwind API, this operation is `POST /v1/accounts/:accountId/posts` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

