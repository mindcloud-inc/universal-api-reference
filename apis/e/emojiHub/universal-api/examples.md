# EmojiHub Universal API Examples

These examples use the MindCloud API key and EmojiHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Emoji

Retrieves a random emoji from EmojiHub.

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

Example response:

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

See the full [Get Random Emoji action reference](actions/get-random-emoji.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emojiHub/latest/actions/get-random-emoji).
