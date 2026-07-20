# List Computers by Set with PrintNode

Retrieves specific computers from PrintNode by ID set.

## Endpoint

- **Method:** `GET`
- **Path:** `/computers/:computerSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Computers by Set](https://www.printnode.com/en/docs/api/curl#computers-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerSet` | path | `string` | yes | Comma-separated PrintNode computer IDs. |
