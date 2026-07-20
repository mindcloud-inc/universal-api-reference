# EmojiHub: Get Random Emoji By Group

Retrieves a random emoji from a selected EmojiHub group.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-group?connectionId=$CONNECTION_ID&group=activities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "activities"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji-by-group?${params}`, {
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
| `group` | list<string> | yes | Emoji group in kebab-case format. One of: `activities`, `animal-amphibian`, `animal-bird`, `animal-bug`, `animal-mammal`, `animal-marine`, `animal-reptile`, `body`, `cat-face`, `clothing`, `creature-face`, `dishware`, `drink`, `emotion`, `face-negative`, `face-neutral`, `face-positive`, `face-role`, `face-sick`, `family`, `flags`, `food-asian`, `food-fruit`, `food-prepared`, `food-sweet`, `food-vegetable`, `monkey-face`, `objects`, `person`, `person-activity`, `person-gesture`, `person-role`, `plant-flower`, `plant-other`, `skin-tone`, `symbols`, `travel-and-places`. |

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

Through the native EmojiHub API, this operation is `GET /random/group/:group` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-emoji-by-group.md) for the provider-specific parameters and requirements.

