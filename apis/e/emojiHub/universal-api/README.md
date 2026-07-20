# <img src="https://images.mindcloud.co/apps/icons/favicon_1781889595385.png" alt="EmojiHub logo" width="28" height="28"> EmojiHub: Universal API

Browse random emojis and lists by category, group, or search

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emojiHub/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/cheatsnake/emojihub
- **Vendor API docs:** https://github.com/cheatsnake/emojihub

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Emoji](actions/get-random-emoji.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emojiHub/latest/actions/get-random-emoji?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Emoji Categories](actions/list-emoji-categories.md) | GET | Lists all categories available in EmojiHub. |

### Emoji

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Emoji](actions/get-random-emoji.md) | GET | Retrieves a random emoji from EmojiHub. |
| [Get Random Emoji By Category](actions/get-random-emoji-by-category.md) | GET | Retrieves a random emoji from a selected EmojiHub category. |
| [Get Random Emoji By Group](actions/get-random-emoji-by-group.md) | GET | Retrieves a random emoji from a selected EmojiHub group. |
| [Get Similar Emojis](actions/get-similar-emojis.md) | GET | Retrieves emojis similar to a selected emoji name. |
| [List Emojis](actions/list-emojis.md) | GET | Lists all emojis available in EmojiHub. |
| [List Emojis By Category](actions/list-emojis-by-category.md) | GET | Lists emojis in a selected EmojiHub category. |
| [List Emojis By Group](actions/list-emojis-by-group.md) | GET | Lists emojis in a selected EmojiHub group. |
| [Search Emojis](actions/search-emojis.md) | GET | Searches EmojiHub emojis by name. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Emoji Groups](actions/list-emoji-groups.md) | GET | Lists all groups available in EmojiHub. |

