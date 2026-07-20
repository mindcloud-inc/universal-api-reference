# Delete Computers by Set with PrintNode

Deletes specific computers from PrintNode by ID set.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/computers/:computerSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Delete Computers by Set](https://www.printnode.com/en/docs/api/curl#computers-removing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerSet` | path | `string` | yes | Comma-separated PrintNode computer IDs. |
