# EmojiHub: Get Similar Emojis

Retrieves emojis similar to a selected emoji name.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-similar-emojis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-similar-emojis?connectionId=$CONNECTION_ID&name=cat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "cat"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-similar-emojis?${params}`, {
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
| `name` | string | yes | Emoji name used to find similar matches. Example: `cat`. |

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

Through the native EmojiHub API, this operation is `GET /similar/:name` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-similar-emojis.md) for the provider-specific parameters and requirements.

