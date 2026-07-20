# List Transaction Documents with Docage

Downloads all documents from a Docage transaction.

## Endpoint

- **Method:** `GET`
- **Path:** `/Transactions/GetTransactionFiles/:id`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [List Transaction Documents](https://documentation.docage.com/t%C3%A9l%C3%A9charger-tous-les-documents-dune-transaction-23280557e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Docage transaction ID. |
