# List Workflow Summaries with OfficeClip

Retrieves workflow summaries from OfficeClip.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/workflow-summary`
- **Base URL:** `https://app.officeclip.com`
- **Official documentation:** [List Workflow Summaries](https://app.officeclip.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | query | `string` | yes | Required OfficeClip workflow entity type token. |
| `entityId` | query | `string` | yes | Required OfficeClip workflow entity serial id. |
| `stageId` | query | `number` | yes | Required OfficeClip workflow stage id. |
