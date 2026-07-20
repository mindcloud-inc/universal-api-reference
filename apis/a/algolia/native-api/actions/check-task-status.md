# Check Task Status with Algolia

Retrieves a task status from Algolia.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes/:indexName/task/:taskID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Check Task Status](https://www.algolia.com/doc/rest-api/search/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexName` | path | `string` | yes | The name of the Algolia index. |
| `taskID` | path | `number` | yes | The task identifier returned by an index operation. |
