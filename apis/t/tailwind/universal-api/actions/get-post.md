# Tailwind: Get Post

Retrieves a post from Tailwind.

```
GET https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/get-post?connectionId=$CONNECTION_ID&accountId=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/get-post?${params}`, {
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
| `accountId` | string | yes | Pinterest account ID. |
| `postId` | string | yes | Tailwind post ID. |

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

Through the native Tailwind API, this operation is `GET /v1/accounts/:accountId/posts/:postId` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

