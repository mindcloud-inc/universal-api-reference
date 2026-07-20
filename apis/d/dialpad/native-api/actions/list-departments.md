# List Departments with Dialpad

## Endpoint

- **Method:** `GET`
- **Path:** `/departments`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Departments](https://developers.dialpad.com/reference/departmentslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `office_id` | query | `number` | no | Filter departments by Dialpad office ID. |
| `name_search` | query | `string` | no | Filter departments by name substring. |
| `cursor` | query | `string` | no | Pagination cursor from a previous Dialpad departments response. |
