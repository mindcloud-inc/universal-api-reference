# Retrieve a Synonym with Algolia

Retrieves an existing synonym from Algolia.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes/:indexName/synonyms/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve a Synonym](https://www.algolia.com/doc/rest-api/search/get-synonym)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to retrieve the synonym. |
| `objectID` | path | `string` | yes | Unique identifier of the synonym object. |
