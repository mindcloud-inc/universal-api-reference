# Upload attachment with Qase

Uploads an attachment to Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachment/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Upload attachment](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `file` | body | `file` | no | Attachment file upload. |
