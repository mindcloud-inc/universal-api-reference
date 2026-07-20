# Cancel Printer Print Jobs by Set with PrintNode

Cancels specific undelivered print jobs for specific printers in PrintNode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/printers/:printerSet/printjobs/:printJobSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Cancel Printer Print Jobs by Set](https://www.printnode.com/en/docs/api/curl#printjobs-removing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
| `printJobSet` | path | `string` | yes | Comma-separated PrintNode print job IDs. |
