# List Computer Printers with PrintNode

Retrieves printers for specific computers from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/computers/:computerSet/printers`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Computer Printers](https://www.printnode.com/en/docs/api/curl#printers-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerSet` | path | `string` | yes | Comma-separated PrintNode computer IDs. |
