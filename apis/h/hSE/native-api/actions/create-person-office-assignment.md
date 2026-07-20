# Create PersonOffice Assignment with 4HSE

Creates a new person-office assignment in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person-office/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create PersonOffice Assignment](https://docs.4hse.com/en/api/personoffice/#operation-createPersonOffice-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `office_id` | body | `string` | yes | Office ID. |
| `person_id` | body | `string` | yes | Person ID. |
| `project_id` | body | `string` | yes | Project ID. |
