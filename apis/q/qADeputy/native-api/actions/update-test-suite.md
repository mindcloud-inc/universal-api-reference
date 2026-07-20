# Update Test Suite with QADeputy

Updates an existing test suite in QADeputy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/test-suites/:testSuiteId`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Update Test Suite](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testSuiteId` | path | `number` | yes | Required QADeputy test_suite_id to update. |
| `name` | body | `string` | no | Updated test suite name. |
| `description` | body | `string` | no | Updated test suite description. |
| `product` | body | `number` | no | QADeputy product ID for the test suite. |
