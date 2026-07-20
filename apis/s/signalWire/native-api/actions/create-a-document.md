# Create a Document with SignalWire

Creates a new document in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasphere/documents`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create a Document](https://signalwire.com/docs/apis/rest/documents/create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max_sentences_per_chunk` | body | `number` | no | Maximum number of sentences per chunk. |
| `chunking_strategy` | body | `string` | no | Strategy for chunking the document |
| `split_newlines` | body | `boolean` | no | Whether to split chunks on new lines.     **Default value:** `false` |
| `url` | body | `string` | yes | URL of the document. |
| `tags[]` | body | `array<string>` | no | Document tags. |
