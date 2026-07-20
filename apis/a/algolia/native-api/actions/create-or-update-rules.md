# Create or Update Rules with Algolia

Creates or updates multiple rules in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/rules/batch`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Create or Update Rules](https://www.algolia.com/doc/rest-api/search/save-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to perform the batch operation. |
| `forwardToReplicas` | query | `boolean` | no | Whether changes are applied to replica indices. |
| `clearExistingRules` | query | `boolean` | no | Whether existing rules should be cleared before the batch write. |
| `rules[]` | body | `array<object>` | yes | Array of rule objects to create or update. |
