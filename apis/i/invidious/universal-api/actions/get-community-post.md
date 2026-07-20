# Invidious: Get Community Post



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post?connectionId=$CONNECTION_ID&id=Ugkx..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "Ugkx..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post?${params}`, {
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
| `channelId` | string | no | Channel UCID for the post. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |
| `id` | string | yes | Community post ID. Example: `Ugkx...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
      "content": "string",
      "postId": "string",
      "publishedText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `content` | string |  |
| `postId` | string |  |
| `publishedText` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /post/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-community-post.md) for the provider-specific parameters and requirements.

