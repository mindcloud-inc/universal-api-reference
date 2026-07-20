# List Workflow Transition Statuses with Intradesk

Retrieves workflow transition statuses from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/changes/api/Rules/transitionstatuses/{workflowId}`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [List Workflow Transition Statuses](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Rules/get_api_Rules_transitionstatuses__workflowId_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier from Intradesk Rules API path. |
