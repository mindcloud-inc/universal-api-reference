# Add Words To Wordlist with Moderation API

Adds words to a wordlist in Moderation API.

## Endpoint

- **Method:** `POST`
- **Path:** `/wordlist/:id/words`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Add Words To Wordlist](https://docs.moderationapi.com/api-reference/wordlist/add-words-to-wordlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the wordlist to add words to |
| `words[]` | body | `array<string>` | yes | Array of words to add to the wordlist. Duplicate words will be ignored. |
