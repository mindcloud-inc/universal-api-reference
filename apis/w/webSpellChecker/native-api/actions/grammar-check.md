# Grammar Check with WebSpellChecker

Checks text for grammar issues in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Grammar Check](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Grammar%2Bcheck%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slang` | query | `string` | no | Language code to use for grammar checks. |
| `text` | query | `string` | yes | The text to grammar-check. |
