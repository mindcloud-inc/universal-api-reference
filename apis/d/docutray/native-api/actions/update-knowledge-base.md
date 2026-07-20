# Update Knowledge Base with Docutray

## Endpoint

- **Method:** `PUT`
- **Path:** `api/knowledge-bases/:id`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Update Knowledge Base](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `name` | body | `string` | no | New name for the knowledge base |
| `description` | body | `string` | no | New description for the knowledge base |
| `schema` | body | `object` | no | Updated JSON schema for documents |
| `indexingPreferences` | body | `object` | no | Updated indexing preferences |
| `isActive` | body | `boolean` | no | Active status of the knowledge base |
