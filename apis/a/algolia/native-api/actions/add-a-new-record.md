# Add a New Record with Algolia

Creates a new record in an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Add a New Record](https://www.algolia.com/doc/rest-api/search/save-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `name` | body | `string` | yes | Record name or title. |
| `objectID` | body | `string` | no | Unique identifier for the record. Omit it to let Algolia generate one. |
| `category` | body | `string` | no | Category value for faceting or filtering. |
| `brand` | body | `string` | no | Brand value for the record. |
| `color` | body | `string` | no | Color value for the record. |
| `price` | body | `number` | no | Numeric price for the record. |
| `isPublished` | body | `boolean` | no | Whether the record is published. |
| `tags[]` | body | `array<string>` | no | Tag values for the record. |
