# Add Knowledge Base Sources with Retell AI

Adds sources to a knowledge base in Retell AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-knowledge-base-sources/{knowledge_base_id}`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Add Knowledge Base Sources](https://docs.retellai.com/api-references/add-knowledge-base-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_files[]` | body | `array<file>` | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledge_base_id` | path | `string` | yes | — |
| `knowledge_base_texts[]` | body | `array<object>` | no | Texts to add to the knowledge base. |
| `knowledge_base_urls[]` | body | `array<string>` | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |
| `knowledge_base_texts[]` | body | `array<object>` | no | Texts to add to the knowledge base. |
| `knowledge_base_texts[]` | body | `array<object>` | no | Texts to add to the knowledge base. |
| `knowledge_base_texts[].title` | body | `string` | yes | Title of the text. |
| `knowledge_base_texts[].text` | body | `string` | yes | Text to add to the knowledge base. |
| `knowledge_base_files[]` | body | `array<file>` | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledge_base_files[]` | body | `array<file>` | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledge_base_urls[]` | body | `array<string>` | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |
| `knowledge_base_urls[]` | body | `array<string>` | no | URLs to be scraped and added to the knowledge base. Must be valid urls. |
