# Search Documents with SignalWire

Searches documents in SignalWire by query string.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasphere/documents/search`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Search Documents](https://signalwire.com/docs/apis/rest/documents/search-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | no | Document tags. |
| `document_id` | body | `string` | no | Unique ID of a Document. |
| `query_string` | body | `string` | yes | Search term. |
| `distance` | body | `number` | no | Specifies how closely related the query is to the document. Low distance means high relevance and similarity. High distance means low relevance and similarity. |
| `count` | body | `number` | no | Specifies number of returned Chunks. |
| `language` | body | `string` | no | Language of the Document. |
| `pos_to_expand[]` | body | `array<string>` | no | Part of Speech considered for expansion or analysis. |
| `max_synonyms` | body | `number` | no | Maximum number of synonyms to consider. |
