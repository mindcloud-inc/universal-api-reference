# Create or Replace a Synonym with Algolia

Creates or replaces a synonym in Algolia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1/indexes/:indexName/synonyms/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Create or Replace a Synonym](https://www.algolia.com/doc/rest-api/search/save-synonym)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to perform the operation. |
| `objectID` | path | `string` | yes | Unique identifier of the synonym object in the request path. |
| `forwardToReplicas` | query | `boolean` | no | Whether changes are applied to replica indices. |
| `objectID` | body | `string` | yes | Unique identifier of the synonym object in the request body. |
| `type` | body | `string` | yes | Synonym type. |
| `synonyms[]` | body | `array<string>` | no | Words or phrases considered equivalent. |
| `input` | body | `string` | no | Query word or phrase for one-way synonyms. |
| `word` | body | `string` | no | Query word or phrase for alternative corrections. |
| `corrections[]` | body | `array<string>` | no | Words to be matched in records for alternative corrections. |
| `placeholder` | body | `string` | no | Placeholder token to put inside records. |
| `replacements[]` | body | `array<string>` | no | Query words that will match the placeholder token. |
