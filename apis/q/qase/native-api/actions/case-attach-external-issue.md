# Attach the external issues to the test cases with Qase

Attaches external issues to test cases in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/case/:code/external-issue/attach`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Attach the external issues to the test cases](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `type` | body | `string` | yes | Required request field type. |
| `links[]` | body | `array<object>` | yes | Required request field links. |
