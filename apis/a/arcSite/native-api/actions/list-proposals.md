# List Proposals with ArcSite

Retrieves proposal records from your ArcSite organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/proposals`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [List Proposals](https://dev.arcsite.com/#query-proposals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Project ID to filter proposals. |
