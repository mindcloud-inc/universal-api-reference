# Create Webset with Exa

Creates a new webset in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/websets`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Create Webset](https://exa.ai/docs/websets/api/websets/create-a-webset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `object` | no | Create initial search for the Webset. |
| `import` | body | `string` | no | Attach/load data from existing Imports or Websets into this Webset. For CSV Imports, this schedules ingestion and creates a staging pool of items (ImportItems do not automatically appear as Webset Items; searches create Webset Items). This does not filter searches. To filter a search to only look within an Import or Webset, use search.scope instead. |
| `enrichments` | body | `string` | no | Add enrichments to extract additional data from found items.  Enrichments automatically search for and extract specific information (like contact details, funding data, employee counts, etc.) from each item added to your Webset. |
| `exclude` | body | `string` | no | Global exclusion sources (existing imports or websets) that apply to all operations within this Webset. Any results found within these sources will be omitted across all search and import operations. |
| `externalId` | body | `string` | no | The external identifier for the webset.  You can use this to reference the Webset by your own internal identifiers. |
| `metadata` | body | `string` | no | Set of key-value pairs you want to associate with this object. |
