# Detach the external issues from the test cases with Qase

Detaches external issues from test cases in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/case/:code/external-issue/detach`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Detach the external issues from the test cases](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `type` | body | `string` | yes | Required request field type. |
| `links[]` | body | `array<object>` | yes | Required request field links. |
