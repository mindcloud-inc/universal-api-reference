# EmojiHub: List Emoji Groups

Lists all groups available in EmojiHub.

```
GET https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/list-emoji-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmojiHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/list-emoji-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/list-emoji-groups?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Emoji group label returned by EmojiHub. |

## Native endpoint

Through the native EmojiHub API, this operation is `GET /groups` (base URL `https://emojihub.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-emoji-groups.md) for the provider-specific parameters and requirements.

