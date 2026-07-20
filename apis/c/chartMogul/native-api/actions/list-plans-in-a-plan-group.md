# List Plans in a Plan Group with ChartMogul

Retrieves plans in a plan group from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/plan_groups/:planGroupUuid/plans`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [List Plans in a Plan Group](https://dev.chartmogul.com/reference/plan-groups/list-plans/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planGroupUuid` | path | `string` | yes | The ChartMogul UUID of the plan group whose plans you want to list. |
