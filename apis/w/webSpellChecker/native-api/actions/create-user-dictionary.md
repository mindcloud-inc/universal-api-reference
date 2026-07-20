# Create User Dictionary with WebSpellChecker

Creates a new user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Create User Dictionary](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the user dictionary to create. |
| `wordlist` | query | `string` | no | Comma-separated list of words to seed in the new dictionary. |
