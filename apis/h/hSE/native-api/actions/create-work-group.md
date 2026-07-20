# Create Work Group with 4HSE

Creates a new work group in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/work-group/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Work Group](https://docs.4hse.com/en/api/workgroup/#operation-createWorkGroup-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Work group name. Maximum length: 255. |
| `office_id` | body | `string` | yes | Office ID. |
| `code` | body | `string` | no | Work group code. Maximum length: 50. |
| `work_group_type` | body | `string` | no | Type of work group. Maximum length: 50. |
