# Update PersonOffice Assignment with 4HSE

Updates an existing person-office assignment in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/person-office/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update PersonOffice Assignment](https://docs.4hse.com/en/api/personoffice/#operation-updatePersonOffice-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PersonOffice assignment ID. |
| `office_id` | body | `string` | yes | Office ID. |
| `person_id` | body | `string` | yes | Person ID. |
| `project_id` | body | `string` | yes | Project ID. |
