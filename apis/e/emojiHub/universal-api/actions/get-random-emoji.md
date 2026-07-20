# EmojiHub: Get Random Emoji

Retrieves a random emoji from EmojiHub.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native EmojiHub API, this operation is `GET /random` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-emoji.md) for the provider-specific parameters and requirements.

