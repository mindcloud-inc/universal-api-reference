# List Print Job States by Set with PrintNode

Retrieves print job states for specific jobs from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/printjobs/:printJobSet/states`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Print Job States by Set](https://www.printnode.com/en/docs/api/curl#printjob-states)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printJobSet` | path | `string` | yes | Comma-separated PrintNode print job IDs. |
