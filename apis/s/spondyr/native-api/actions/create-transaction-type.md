# Create Transaction Type with Spondyr

Creates a new transaction type in Spondyr.

## Endpoint

- **Method:** `POST`
- **Path:** `/TransactionType`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Create Transaction Type](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The new transaction type name. |
| `TemplateJSON` | body | `string` | yes | Sample JSON payload that defines the transaction type schema. |
