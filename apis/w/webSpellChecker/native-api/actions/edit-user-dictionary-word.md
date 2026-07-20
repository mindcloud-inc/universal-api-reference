# Edit User Dictionary Word with WebSpellChecker

Replaces a word in a user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Edit User Dictionary Word](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the dictionary to update. |
| `word` | query | `string` | yes | Existing dictionary word to replace. |
| `new_word` | query | `string` | yes | Replacement word. |
