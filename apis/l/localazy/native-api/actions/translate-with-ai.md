# Translate With AI with Localazy

Creates AI translations for source strings in Localazy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/ai`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Translate With AI](https://localazy.com/docs/api/ai-translation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `from` | body | `string` | yes | Source locale code. |
| `to` | body | `string` | yes | Target locale code. |
| `items[]` | body | `array<object>` | yes | Translation items to submit. |
| `items[].key` | body | `string` | no | Optional localization key. |
| `items[].source` | body | `string` | yes | Source text to translate. |
| `items[].comment` | body | `string` | no | Optional translation context. |
| `items[].lengthLimit` | body | `number` | no | Maximum translation length in characters. |
| `fallback` | body | `string` | no | Fallback machine translation engine. |
