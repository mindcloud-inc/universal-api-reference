# List Transformations with Fivetran

Retrieves transformations from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/transformations`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [List Transformations](https://fivetran.com/docs/rest-api/api-reference/transformation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | Filter transformations by group ID. |
| `project_id` | query | `string` | no | Filter transformations by dbt Core project ID. |
| `type` | query | `string` | no | Filter transformations by type. |
