# Deanonymize Text with Wikibot

Deanonymizes text in Wikibot.

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/deanonymize`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Deanonymize Text](https://wikibot.pro/docs/api/deanonymize)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `anonymized_text` | body | `string` | yes | Anonymized text that contains replacement fake values. |
| `replacements[]` | body | `array<object>` | yes | Replacement map entries with fake and original values. Send multiple values as a array. |
