# Update Wordlist with Moderation API

Updates a wordlist in Moderation API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/wordlist/:id`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Update Wordlist](https://docs.moderationapi.com/api-reference/wordlist/update-wordlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the wordlist to update |
| `name` | body | `string` | no | New name for the wordlist |
| `key` | body | `string` | no | New key for the wordlist |
| `description` | body | `string` | no | New description for the wordlist |
| `words[]` | body | `array<string>` | no | New words for the wordlist. Replace the existing words with these new ones. Duplicate words will be ignored. |
| `strict` | body | `boolean` | no | Deprecated. Now using threshold in project settings. |
