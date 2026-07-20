# Add User Dictionary Word with WebSpellChecker

Adds a word to a user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Add User Dictionary Word](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Using%2BWebSpellChecker%2BServer%2BWeb%2BAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the dictionary to update. |
| `word` | query | `string` | yes | Single word to add to the dictionary. |
