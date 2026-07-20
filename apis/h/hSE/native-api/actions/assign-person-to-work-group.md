# Assign Person To Work Group with 4HSE

Creates a new work group assignment in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/work-group-person/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Assign Person To Work Group](https://docs.4hse.com/en/api/workgroupperson/#operation-createWorkGroupPerson-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `work_group_id` | body | `string` | yes | Work group ID. |
| `person_office_id` | body | `string` | yes | PersonOffice assignment ID. |
| `time_spent_measure` | body | `string` | no | Exposure time value. |
| `unit_of_measure_id` | body | `string` | no | Unit of measure ID. |
