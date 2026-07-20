# Create or Replace a Rule with Algolia

Creates or replaces a rule in Algolia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1/indexes/:indexName/rules/:objectID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Create or Replace a Rule](https://www.algolia.com/doc/rest-api/search/save-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | Name of the index on which to perform the operation. |
| `objectID` | path | `string` | yes | Unique identifier of the rule object in the request path. |
| `forwardToReplicas` | query | `boolean` | no | Whether changes are applied to replica indices. |
| `objectID` | body | `string` | yes | Unique identifier of the rule object in the request body. |
| `consequence` | body | `object` | yes | Effect of the rule as a JSON object. |
| `conditions[]` | body | `array<object>` | no | Conditions that trigger the rule as an array of JSON objects. |
| `description` | body | `string` | no | Description to help identify this rule. |
| `enabled` | body | `boolean` | no | Whether the rule is enabled. |
| `tags[]` | body | `array<string>` | no | Tags attached to the rule. |
| `validity[]` | body | `array<object>` | no | Validity windows for the rule. |
| `scope` | body | `string` | no | The scope of the rule. |
