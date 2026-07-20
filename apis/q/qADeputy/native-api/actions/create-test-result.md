# Create Test Result with QADeputy

Creates a test result for a QADeputy test case.

## Endpoint

- **Method:** `POST`
- **Path:** `/test-cases/:testCaseId/test-results`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Create Test Result](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testCaseId` | path | `number` | yes | Required QADeputy test_case_id receiving a test result. |
| `test_case_status` | body | `number` | yes | QADeputy test case status ID/value for the result. |
| `actual_result` | body | `string` | no | Actual result notes. |
| `created_by_user_id` | body | `number` | yes | QADeputy user ID creating the result. |
| `test_run` | body | `number` | yes | QADeputy test run ID for the result. |
