# Create Corpus with Vectara

Creates a new corpus in Vectara.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corpora`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Create Corpus](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Unique key for the new corpus. |
| `name` | body | `string` | no | Display name for the corpus. |
| `description` | body | `string` | no | Description of the corpus. |
| `save_history` | body | `boolean` | no | Whether queries to this corpus should be saved by default. |
| `queries_are_answers` | body | `boolean` | no | Treat queries as answers instead of questions. |
| `documents_are_questions` | body | `boolean` | no | Treat indexed documents as questions instead of answers. |
| `encoder_name` | body | `string` | no | Encoder name to use for the corpus. |
| `filter_attributes[]` | body | `array<object>` | no | Filter attribute definitions for the corpus. |
| `custom_dimensions[]` | body | `array<object>` | no | Custom dimension definitions for the corpus. |
