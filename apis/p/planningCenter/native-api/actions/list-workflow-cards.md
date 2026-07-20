# List Workflow Cards with Planning Center

Retrieves workflow cards for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/workflow_cards`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Workflow Cards](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow_card)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | path | `number` | yes | Person ID |
| `include` | query | `string` | no | Include associated resources |
| `order` | query | `string` | no | Sort returned workflow cards |
| `where` | query | `object` | no | Equality filters for workflow card fields |
| `where[assignee_id]` | query | `number` | no | Query on a related assignee |
| `where[overdue]` | query | `boolean` | no | Query on a specific overdue value |
| `where[stage]` | query | `string` | no | Query on a specific stage |
