# List Printers by Set with PrintNode

Retrieves specific printers from PrintNode by ID set.

## Endpoint

- **Method:** `GET`
- **Path:** `/printers/:printerSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Printers by Set](https://www.printnode.com/en/docs/api/curl#printers-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
