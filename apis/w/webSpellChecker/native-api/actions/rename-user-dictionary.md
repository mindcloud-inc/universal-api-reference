# Rename User Dictionary with WebSpellChecker

Renames a user dictionary in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Rename User Dictionary](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Existing dictionary name. |
| `new_name` | query | `string` | yes | New name for the dictionary. |
