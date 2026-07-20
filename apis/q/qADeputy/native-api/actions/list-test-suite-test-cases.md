# List Test Suite Test Cases with QADeputy

Retrieves test cases in a QADeputy test suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-suites/:testSuiteId/test-cases`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Suite Test Cases](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testSuiteId` | path | `number` | yes | Required QADeputy test_suite_id whose test cases should be listed. |
| `test_case_status` | query | `list` | no | Optional test case status filter. The docs show archived as an example. Accepted values: `0`, `1`. |
| `test_feature` | query | `number` | no | Optional test feature filter ID. |
