# Check Text with WebSpellChecker

Checks text for spelling, grammar, and style issues in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Check Text](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Using%2BCloud%2BWebSpellChecker%2BAPI)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | The text to check. |
| `lang` | query | `string` | no | Language code to use for checking. |
| `disable_spelling` | query | `string` | no | Disable spelling checks. |
| `disable_grammar` | query | `string` | no | Disable grammar checks. |
