# List Test Run Test Cases with QADeputy

Retrieves test cases in a QADeputy test run.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-runs/:testRunId/test-cases`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Run Test Cases](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testRunId` | path | `number` | yes | Required QADeputy test_run_id whose test cases should be listed. |
