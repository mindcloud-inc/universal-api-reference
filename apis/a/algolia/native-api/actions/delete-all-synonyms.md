# Delete All Synonyms with Algolia

Deletes all synonyms from an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/synonyms/clear`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete All Synonyms](https://www.algolia.com/doc/rest-api/search/clear-synonyms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Index name from which to delete all synonyms. |
| `forwardToReplicas` | query | `boolean` | no | Whether to forward the deletion to replicas. |
