# Create Knowledge Base with Retell AI

Creates a knowledge base in Retell AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-knowledge-base`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Create Knowledge Base](https://docs.retellai.com/api-references/create-knowledge-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_files[]` | body | `array<file>` | no | Files to add to the knowledge base. Limit to 25 files, where each file is limited to 50MB. |
| `knowledge_base_name` | body | `string` | yes | Name of the knowledge base. Must be less than 40 characters. |
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
| `enable_auto_refresh` | body | `boolean` | no | Whether to enable auto refresh for the knowledge base urls. If set to true, will retrieve the data from the specified url every 12 hours. |
| `max_chunk_size` | body | `number` | no | Maximum number of characters per chunk when splitting knowledge base. Default is 2000. content. Immutable after creation. |
| `min_chunk_size` | body | `number` | no | Minimum number of characters per chunk. Chunks smaller than this will be merged with adjacent chunks. Must be less than max_chunk_size. Immutable after creation. Default is 400. |
