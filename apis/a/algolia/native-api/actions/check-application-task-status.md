# Check Application Task Status with Algolia

Retrieves an application task status from Algolia.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/task/:taskID`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Check Application Task Status](https://www.algolia.com/doc/rest-api/search/get-app-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | path | `number` | yes | The application task identifier returned by a multi-index or settings operation. |
