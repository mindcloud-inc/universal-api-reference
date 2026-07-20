# Cancel Printer Print Jobs with PrintNode

Cancels undelivered print jobs for specific printers in PrintNode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/printers/:printerSet/printjobs`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Cancel Printer Print Jobs](https://www.printnode.com/en/docs/api/curl#printjobs-removing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerSet` | path | `string` | yes | Comma-separated PrintNode printer IDs. |
