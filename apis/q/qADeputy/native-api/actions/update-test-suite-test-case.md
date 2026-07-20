# Update Test Suite Test Case with QADeputy

Updates a test case in a QADeputy test suite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/test-suites/:testSuiteId/test-cases/:testCaseId`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Update Test Suite Test Case](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testSuiteId` | path | `number` | yes | Required QADeputy test_suite_id. |
| `testCaseId` | path | `number` | yes | Required QADeputy test_case_id to update. |
| `name` | body | `string` | no | Updated test case name. |
| `preconditions` | body | `string` | no | Updated preconditions for the test case. |
| `expected_results` | body | `string` | no | Updated expected results for the test case. |
| `test_case_steps` | body | `string` | no | Updated test case steps. |
| `specifications` | body | `string` | no | Updated specifications URL or reference. |
| `time` | body | `string` | no | Estimated test case time in QADeputy's documented HH:mm format. |
