# List Printer Print Jobs by Set with PrintNode

Retrieves specific print jobs for specific printers from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/printers/:printerSet/printjobs/:printJobSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Printer Print Jobs by Set](https://www.printnode.com/en/docs/api/curl#printjob-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
| `printJobSet` | path | `string` | yes | Comma-separated PrintNode print job IDs. |
