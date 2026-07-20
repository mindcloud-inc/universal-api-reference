# Delete All Rules with Algolia

Deletes all rules from an Algolia index.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/:indexName/rules/clear`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Delete All Rules](https://www.algolia.com/doc/rest-api/search/clear-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Index name from which to delete all rules. |
| `forwardToReplicas` | query | `boolean` | no | Whether to forward the deletion to replicas. |
