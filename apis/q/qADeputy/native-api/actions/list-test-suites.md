# List Test Suites with QADeputy

Retrieves test suites from QADeputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-suites`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Suites](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `test_suite_status` | query | `list` | no | Optional test suite status filter. The API defaults to active. Accepted values: `0`, `1`. |
