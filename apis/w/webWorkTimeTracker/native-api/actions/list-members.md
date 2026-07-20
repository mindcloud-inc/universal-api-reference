# List Members with WebWork Time Tracker

Retrieves workspace members from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/members`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Members](https://api-docs.webwork-tracker.com/api/members/getmembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `email` | query | `string` | no |
| `status` | query | `string` | no |
| `role` | query | `string` | no |
