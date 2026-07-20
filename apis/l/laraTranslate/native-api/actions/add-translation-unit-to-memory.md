# Add translation unit to memory with Lara Translate

Adds a translation unit to a Lara Translate memory.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Add translation unit to memory](https://developers.laratranslate.com/docs/manage-translation-memories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string<string>` | yes | The translation memory ID to receive the translation unit. |
| `source` | body | `string` | yes | Source language code for the sentence. |
| `target` | body | `string` | yes | Target language code for the translation. |
| `sentence` | body | `string` | yes | Source sentence. |
| `translation` | body | `string` | yes | Translated sentence. |
| `tuid` | body | `string` | no | Optional translation unit identifier. |
| `sentence_before` | body | `string` | no | Optional sentence before the source sentence for context. |
| `sentence_after` | body | `string` | no | Optional sentence after the source sentence for context. |
