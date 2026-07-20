# Get Test Suite Test Case with QADeputy

Retrieves a test case from a QADeputy test suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-suites/:testSuiteId/test-cases/:testCaseId`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Get Test Suite Test Case](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testSuiteId` | path | `number` | yes | Required QADeputy test_suite_id. |
| `testCaseId` | path | `number` | yes | Required QADeputy test_case_id. |
