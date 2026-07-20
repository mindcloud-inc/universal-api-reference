# Update Test Run Test Case with QADeputy

Updates a test case in a QADeputy test run.

## Endpoint

- **Method:** `PUT`
- **Path:** `/test-runs/:testRunId/test-cases/:testCaseId`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Update Test Run Test Case](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testRunId` | path | `number` | yes | Required QADeputy test_run_id. |
| `testCaseId` | path | `number` | yes | Required QADeputy test_case_id in the test run. |
| `test_case_status` | body | `number` | yes | QADeputy test case status ID/value for this run test case. |
| `actual_result` | body | `string` | no | Actual result notes for the test case in this run. |
