# Create a new plan with Qase

Creates a new test plan in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/plan/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new plan](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
| `cases[]` | body | `array<number>` | yes | Required request field cases. |
