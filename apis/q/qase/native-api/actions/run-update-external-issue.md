# Update external issues for runs with Qase

Updates external issue links for test runs in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/run/:code/external-issue`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update external issues for runs](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `type` | body | `string` | yes | Required request field type. |
| `links[]` | body | `array<object>` | yes | Array of external issue links. Each test run (run_id) can have only one external issue link. |
