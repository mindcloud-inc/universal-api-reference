# Create a new shared parameter with Qase

Creates a new shared parameter in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/shared_parameter`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new shared parameter](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Required request field title. |
| `type` | body | `string` | yes | Required request field type. |
| `is_enabled_for_all_projects` | body | `boolean` | yes | Required request field is_enabled_for_all_projects. |
| `parameters` | body | `string` | yes | Required request field parameters. |
