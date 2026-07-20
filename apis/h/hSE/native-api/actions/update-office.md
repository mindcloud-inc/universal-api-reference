# Update Office with 4HSE

Updates an existing office in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/office/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update Office](https://docs.4hse.com/en/api/office/#operation-updateOffice-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The office_id to update. |
| `project_id` | body | `string` | yes | The project this office belongs to. |
| `name` | body | `string` | yes | Name of the office or work location. Maximum length: 255. |
| `description` | body | `string` | no | Optional free-text description. |
| `code` | body | `string` | no | Alternative identifier code for the office. Maximum length: 50. |
| `office_type_icon` | body | `string` | no | Visual type of the office. |
