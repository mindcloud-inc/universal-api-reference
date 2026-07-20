# Add User Dictionary Words with WebSpellChecker

Adds words to a user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Add User Dictionary Words](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the dictionary to update. |
| `wordlist` | query | `string` | yes | Comma-separated words to add to the dictionary. |
