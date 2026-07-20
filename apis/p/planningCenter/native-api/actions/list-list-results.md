# List List Results with Planning Center

Retrieves results for a list in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/lists/:list_id/list_results`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List List Results](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list_result)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List ID |
| `order` | query | `string` | no | Sort returned list results |
