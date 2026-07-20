# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-laratranslate-com-48x48_1777036668449.png" alt="Lara Translate logo" width="28" height="28"> Lara Translate: Universal API

Use Lara Translate's hosted MCP tool surface to translate text, detect language, and manage translation memories.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/laraTranslate/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://laratranslate.com
- **Vendor API docs:** https://developers.laratranslate.com/docs/getting-started-with-mcp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List supported languages](actions/list-supported-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Language Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect language](actions/detect-language.md) | GET | Detects the source language of text in Lara Translate. |

### Memory Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Check memory import status](actions/check-memory-import-status.md) | GET | Retrieves the status of a Lara Translate memory import. |
| [Import TMX into memory](actions/import-tmx-into-memory.md) | POST | Imports a TMX file into a Lara Translate memory. |

### Supported Language

| Action | Method | Description |
| --- | --- | --- |
| [List supported languages](actions/list-supported-languages.md) | GET | Retrieves supported languages from Lara Translate. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate text](actions/translate-text.md) | GET | Translates text from one language to another in Lara Translate. |

### Translation Memory

| Action | Method | Description |
| --- | --- | --- |
| [Create translation memory](actions/create-translation-memory.md) | POST | Creates a new translation memory in Lara Translate. |
| [Delete translation memory](actions/delete-translation-memory.md) | DELETE | Deletes an existing translation memory from Lara Translate. |
| [List translation memories](actions/list-translation-memories.md) | GET | Retrieves translation memories from Lara Translate. |
| [Rename translation memory](actions/rename-translation-memory.md) | PUT | Updates an existing translation memory in Lara Translate. |

### Translation Unit

| Action | Method | Description |
| --- | --- | --- |
| [Add translation unit to memory](actions/add-translation-unit-to-memory.md) | POST | Adds a translation unit to a Lara Translate memory. |
| [Delete translation unit from memory](actions/delete-translation-unit-from-memory.md) | DELETE | Deletes translation units from a Lara Translate memory. |

