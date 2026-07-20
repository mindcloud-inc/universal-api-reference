# EmojiHub: Get Random Emoji By Category

Retrieves a random emoji from a selected EmojiHub category.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-category?connectionId=$CONNECTION_ID&category=activities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "activities"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-category?${params}`, {
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
| `category` | list<string> | yes | Emoji category in kebab-case format. One of: `activities`, `animals-and-nature`, `flags`, `food-and-drink`, `objects`, `smileys-and-people`, `symbols`, `travel-and-places`. |

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

Through the native EmojiHub API, this operation is `GET /random/category/:category` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-emoji-by-category.md) for the provider-specific parameters and requirements.

