# List Contracts with WebWork Time Tracker

Retrieves workspace contracts from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Contracts](https://api-docs.webwork-tracker.com/api/contracts/getcontracts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `project_id` | query | `number` | no |
| `user_id` | query | `number` | no |
| `status` | query | `string` | no |
