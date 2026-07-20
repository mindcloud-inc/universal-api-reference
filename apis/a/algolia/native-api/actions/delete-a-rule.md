# Delete a Rule with Algolia

Deletes an existing rule from Algolia.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1/indexes/:indexName/rules/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete a Rule](https://www.algolia.com/doc/rest-api/search/delete-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Index name that contains the rule. |
| `objectID` | path | `string` | yes | Unique identifier of the rule object. |
| `forwardToReplicas` | query | `boolean` | no | Whether to forward the deletion to replicas. |
