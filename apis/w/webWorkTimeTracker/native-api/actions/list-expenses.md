# List Expenses with WebWork Time Tracker

Retrieves expenses from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/expenses`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Expenses](https://api-docs.webwork-tracker.com/api/expenses/getexpenses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
