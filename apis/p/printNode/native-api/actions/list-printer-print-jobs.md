# List Printer Print Jobs with PrintNode

Retrieves print jobs for specific printers from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/printers/:printerSet/printjobs`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Printer Print Jobs](https://www.printnode.com/en/docs/api/curl#printjob-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
