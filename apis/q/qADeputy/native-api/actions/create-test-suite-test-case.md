# Create Test Suite Test Case with QADeputy

Creates a test case in a QADeputy test suite.

## Endpoint

- **Method:** `POST`
- **Path:** `/test-suites/:testSuiteId/test-cases`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Create Test Suite Test Case](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testSuiteId` | path | `number` | yes | Required QADeputy test_suite_id where the test case will be created. |
| `test_feature_id` | body | `number` | yes | QADeputy test feature ID for the new test case. |
| `name` | body | `string` | yes | New test case name. |
| `preconditions` | body | `string` | no | Preconditions for the new test case. |
| `expected_results` | body | `string` | no | Expected results for the new test case. |
| `test_case_steps` | body | `string` | no | Steps for the new test case. |
| `specifications` | body | `string` | no | Specifications URL or reference. |
| `time` | body | `string` | no | Estimated test case time in QADeputy's documented HH:mm format. |
