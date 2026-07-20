# List Computer Printers by Set with PrintNode

Retrieves specific printers for specific computers from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/computers/:computerSet/printers/:printerSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Computer Printers by Set](https://www.printnode.com/en/docs/api/curl#printers-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerSet` | path | `string` | yes | Comma-separated PrintNode computer IDs. |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
