# List Print Jobs by Set with PrintNode

Retrieves specific print jobs from PrintNode by ID set.

## Endpoint

- **Method:** `GET`
- **Path:** `/printjobs/:printJobSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Print Jobs by Set](https://www.printnode.com/en/docs/api/curl#printjob-viewing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printJobSet` | path | `string` | yes | Comma-separated PrintNode print job IDs. |
