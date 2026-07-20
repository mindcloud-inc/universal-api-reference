# Delete a Synonym with Algolia

Deletes an existing synonym from Algolia.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1/indexes/:indexName/synonyms/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete a Synonym](https://www.algolia.com/doc/rest-api/search/delete-synonym)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Index name that contains the synonym. |
| `objectID` | path | `string` | yes | Unique identifier of the synonym object. |
| `forwardToReplicas` | query | `boolean` | no | Whether to forward the deletion to replicas. |
