# Add or Replace a Record with Algolia

Adds or replaces a record in Algolia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1/indexes/:indexName/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Add or Replace a Record](https://www.algolia.com/doc/rest-api/search/add-or-update-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `objectID` | path | `string` | yes | Unique identifier for the record to create or replace. |
| `name` | body | `string` | yes | Record name or title. |
| `category` | body | `string` | no | Category value for faceting or filtering. |
| `brand` | body | `string` | no | Brand value for the record. |
| `color` | body | `string` | no | Color value for the record. |
| `price` | body | `number` | no | Numeric price for the record. |
| `isPublished` | body | `boolean` | no | Whether the record is published. |
| `tags[]` | body | `array<string>` | no | Tag values for the record. |
