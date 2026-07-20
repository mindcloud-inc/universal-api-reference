# Create Knowledge Base with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/knowledge-bases`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Create Knowledge Base](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique name for the knowledge base |
| `description` | body | `string` | yes | Description of the knowledge base |
| `schema` | body | `object` | yes | Required JSON schema for documents |
| `indexingPreferences` | body | `object` | no | Indexing preferences |
