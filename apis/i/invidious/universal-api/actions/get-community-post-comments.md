# Invidious: Get Community Post Comments



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post-comments?connectionId=$CONNECTION_ID&channelId=UC_x5XG1OV2P6uZZ5FSM9Ttw&id=Ugkx..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw",
  "id": "Ugkx..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-community-post-comments?${params}`, {
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
| `channelId` | string | yes | Channel UCID for the post comments. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |
| `id` | string | yes | Community post ID. Example: `Ugkx...`. |
| `sortBy` | string | no | Comment sort order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentCount": 1,
      "comments": [
        {}
      ],
      "continuation": "string",
      "postId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentCount` | number |  |
| `comments` | array<object> |  |
| `continuation` | string |  |
| `postId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /post/:id/comments` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-community-post-comments.md) for the provider-specific parameters and requirements.

