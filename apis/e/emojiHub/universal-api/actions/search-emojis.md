# EmojiHub: Search Emojis

Searches EmojiHub emojis by name.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/search-emojis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/search-emojis?connectionId=$CONNECTION_ID&query=smile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "smile"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/search-emojis?${params}`, {
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
| `query` | string | yes | Text used to search emoji names. Example: `smile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "group": "string",
      "htmlCode": [
        "string"
      ],
      "name": "Ava Chen",
      "unicode": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Top-level EmojiHub category. |
| `group` | string | EmojiHub group label. |
| `htmlCode` | array<string> | HTML entity codes for the emoji. |
| `name` | string | Emoji display name. |
| `unicode` | array<string> | Unicode code points for the emoji. |

## Native endpoint

Through the native EmojiHub API, this operation is `GET /search` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-emojis.md) for the provider-specific parameters and requirements.

