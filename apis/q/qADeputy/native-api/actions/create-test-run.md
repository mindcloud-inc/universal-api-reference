# Create Test Run with QADeputy

Creates a new test run in QADeputy.

## Endpoint

- **Method:** `POST`
- **Path:** `/test-runs`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Create Test Run](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Test run name. |
| `description` | body | `string` | no | Test run description. |
| `test_suite` | body | `number` | yes | QADeputy test suite ID to create the test run from. |
| `users[]` | body | `array<number>` | no | QADeputy user IDs assigned to the test run. |
| `include_all` | body | `boolean` | no | Whether QADeputy should include all test cases. |
| `test_cases[]` | body | `array<number>` | no | QADeputy test case IDs to include when includeAll is false. |
