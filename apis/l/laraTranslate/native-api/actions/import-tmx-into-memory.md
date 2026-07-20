# Import TMX into memory with Lara Translate

Imports a TMX file into a Lara Translate memory.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Import TMX into memory](https://developers.laratranslate.com/docs/manage-translation-memories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the translation memory to import TMX content into. |
| `tmx_content` | body | `string` | yes | Raw TMX file content. |
