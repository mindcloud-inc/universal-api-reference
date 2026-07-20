# Create Test Suite with QADeputy

Creates a new test suite in QADeputy.

## Endpoint

- **Method:** `POST`
- **Path:** `/test-suites`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [Create Test Suite](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Test suite name. |
| `description` | body | `string` | yes | Test suite description. |
| `product` | body | `number` | yes | QADeputy product ID for the test suite. |
