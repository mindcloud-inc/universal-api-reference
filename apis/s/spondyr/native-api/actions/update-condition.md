# Update Condition with Spondyr

Updates an existing condition for a transaction type in Spondyr.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Condition`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Update Condition](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | body | `string` | yes | The transaction type the condition belongs to. |
| `Condition` | body | `string` | yes | The existing condition name to update. |
| `Name` | body | `string` | yes | The new condition name. |
| `FieldName` | body | `string` | yes | The field name the condition evaluates. |
| `PossibleValues` | body | `string` | yes | The newline-delimited possible values for the condition. |
