# Get User Dictionary with WebSpellChecker

Retrieves a user dictionary wordlist from WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Get User Dictionary](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the dictionary to load. |
