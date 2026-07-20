# Check Spelling with WebSpellChecker

Checks text for spelling errors in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Check Spelling](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Check%2Bspelling%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | The text to spell-check. |
| `slang` | query | `string` | no | Language code to use for spelling. |
