# List Emojis By Category with EmojiHub

Lists emojis in a selected EmojiHub category.

## Endpoint

- **Method:** `GET`
- **Path:** `/all/category/:category`
- **Base URL:** `https://emojihub.yurace.pro/api`
- **Official documentation:** [List Emojis By Category](https://github.com/cheatsnake/emojihub)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | path | `list<string>` | yes | Emoji category in kebab-case format. Accepted values: `activities`, `animals-and-nature`, `flags`, `food-and-drink`, `objects`, `smileys-and-people`, `symbols`, `travel-and-places`. |
