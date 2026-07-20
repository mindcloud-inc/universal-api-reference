# Retrieve a Rule with Algolia

Retrieves an existing rule from Algolia.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes/:indexName/rules/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve a Rule](https://www.algolia.com/doc/rest-api/search/get-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to retrieve the rule. |
| `objectID` | path | `string` | yes | Unique identifier of the rule object. |
