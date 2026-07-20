# Remove Words From Wordlist with Moderation API

Removes words from a wordlist in Moderation API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/wordlist/:id/words`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Remove Words From Wordlist](https://docs.moderationapi.com/api-reference/wordlist/remove-words-from-wordlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the wordlist to remove words from |
| `words[]` | query | `array<string>` | yes | Array of words to remove from the wordlist |
