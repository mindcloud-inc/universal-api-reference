# List Workflow Steps for a Link with Linkbreakers

Retrieves workflow steps for a link in Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/:linkId/workflow-steps`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Workflow Steps for a Link](https://linkbreakers.com/help/api/workflow-steps)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | The ID of the link to list workflow steps for. |
