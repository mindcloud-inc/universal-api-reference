# List Workspaces with Rossum

Retrieves workspaces from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Workspaces](https://rossum.app/api/docs/openapi/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter workspaces by name. |
| `ordering` | query | `string` | no | Sort workspaces by a supported field using Rossum ordering syntax. |
| `organization` | query | `string` | no | Filter workspaces by organization ID. |
