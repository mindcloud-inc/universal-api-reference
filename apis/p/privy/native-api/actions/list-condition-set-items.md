# List Condition Set Items with Privy

Retrieves items from a Privy condition set.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/condition_sets/{{conditionSetId}}/condition_set_items`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [List Condition Set Items](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets~1{condition_set_id}~1condition_set_items/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `condition_set_id` | path | `string` | yes | Privy condition set ID. |
