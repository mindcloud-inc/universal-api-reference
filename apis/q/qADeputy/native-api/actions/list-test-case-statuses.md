# List Test Case Statuses with QADeputy

Retrieves test case statuses from QADeputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/test-case-statuses`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Test Case Statuses](https://apidocs.qadeputy.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status_type` | query | `list` | no | Optional test case status type filter. The docs use predefined_status. Accepted values: `0`. |
