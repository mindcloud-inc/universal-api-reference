# Cancel Print Jobs by Set with PrintNode

Cancels specific undelivered print jobs in PrintNode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/printjobs/:printJobSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Cancel Print Jobs by Set](https://www.printnode.com/en/docs/api/curl#printjobs-removing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printJobSet` | path | `string` | yes | Comma-separated PrintNode print job IDs. |
