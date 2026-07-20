# Update Test Run with QADeputy

Updates an existing test run in QADeputy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/test-runs/:testRunId`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Update Test Run](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testRunId` | path | `number` | yes | Required QADeputy test_run_id to update. |
| `name` | body | `string` | no | Updated test run name. |
| `description` | body | `string` | no | Updated test run description. |
| `users[]` | body | `array<number>` | no | Updated QADeputy user IDs assigned to the test run. |
| `include_all` | body | `boolean` | no | Whether QADeputy should include all test cases. |
| `test_cases[]` | body | `array<number>` | no | Updated QADeputy test case IDs to include when includeAll is false. |
