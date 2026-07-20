# Delete User Dictionary Word with WebSpellChecker

Deletes a word from a user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Delete User Dictionary Word](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Using%2BWebSpellChecker%2BServer%2BWeb%2BAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the dictionary to update. |
| `word` | query | `string` | yes | Single word to remove from the dictionary. |
