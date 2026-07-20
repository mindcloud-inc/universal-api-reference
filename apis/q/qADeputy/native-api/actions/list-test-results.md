# List Test Results with QADeputy

Retrieves test results for a QADeputy test case.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-cases/:testCaseId/test-results`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Results](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testCaseId` | path | `number` | yes | Required QADeputy test_case_id whose results should be listed. |
