# Create Condition with Spondyr

Creates a new condition for a transaction type in Spondyr.

## Endpoint

- **Method:** `POST`
- **Path:** `/Condition`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Create Condition](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | body | `string` | yes | The transaction type the condition belongs to. |
| `Name` | body | `string` | yes | The new condition name. |
| `FieldName` | body | `string` | yes | The field name the condition evaluates. |
| `PossibleValues` | body | `string` | yes | The newline-delimited possible values for the condition. |
