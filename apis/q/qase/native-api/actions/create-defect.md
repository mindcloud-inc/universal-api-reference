# Create a new defect with Qase

Creates a new defect in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/defect/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new defect](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
| `actual_result` | body | `string` | yes | Required request field actual_result. |
| `severity` | body | `number` | yes | Required request field severity. |
