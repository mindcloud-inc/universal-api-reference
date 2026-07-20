# Update Transaction Type with Spondyr

Updates an existing transaction type in Spondyr.

## Endpoint

- **Method:** `PUT`
- **Path:** `/TransactionType`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Update Transaction Type](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | body | `string` | yes | The existing transaction type name to update. |
| `Name` | body | `string` | yes | The new transaction type name. |
| `TemplateJSON` | body | `string` | yes | Sample JSON payload that defines the transaction type schema. |
