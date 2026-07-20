# Add or Update Attributes with Algolia

Adds or updates record attributes in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/:objectID/partial`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Add or Update Attributes](https://www.algolia.com/doc/rest-api/search/partial-update-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `objectID` | path | `string` | yes | Unique identifier for the record. |
| `createIfNotExists` | query | `boolean` | no | Whether to create the record if it does not exist. |
| `name` | body | `string` | no | Record name or title. |
| `category` | body | `string` | no | Category value for faceting or filtering. |
| `brand` | body | `string` | no | Brand value for the record. |
| `color` | body | `string` | no | Color value for the record. |
| `price` | body | `number` | no | Numeric price for the record. |
| `isPublished` | body | `boolean` | no | Whether the record is published. |
| `tags[]` | body | `array<string>` | no | Tag values for the record. |
