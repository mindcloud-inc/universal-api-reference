# List Test Runs with QADeputy

Retrieves test runs from QADeputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-runs`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Runs](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_completed` | query | `list` | no | Optional completion filter. Use 0 for active test runs and 1 for completed test runs; omit to list both. Accepted values: `0`, `1`. |
