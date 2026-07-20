# Execute View with Zendesk

Retrieves results for a Zendesk view.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/:view_id/execute.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Execute View](https://developer.zendesk.com/api-reference/ticketing/business-rules/views/#execute-view)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_id` | path | `number` | yes | View ID |
