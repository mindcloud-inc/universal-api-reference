# Anonymize Text with Wikibot

Anonymizes text in Wikibot.

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/anonymize`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Anonymize Text](https://wikibot.pro/docs/api/anonymize)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Source text to anonymize. |
| `existingReplacements[]` | body | `array<object>` | no | Existing replacement map entries to apply or account for during anonymization. Send multiple values as a array. |
| `ignored_names` | body | `string` | no | Optional names to ignore during anonymization. |
