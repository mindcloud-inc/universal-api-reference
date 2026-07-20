# Create or Replace Synonyms with Algolia

Creates or replaces multiple synonyms in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/synonyms/batch`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Create or Replace Synonyms](https://www.algolia.com/doc/rest-api/search/save-synonyms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to perform the batch operation. |
| `forwardToReplicas` | query | `boolean` | no | Whether changes are applied to replica indices. |
| `replaceExistingSynonyms` | query | `boolean` | no | Whether to replace all synonyms in the index with the ones in this request. |
| `synonymObjects[]` | body | `array<object>` | yes | Array of synonym objects to create or replace. |
