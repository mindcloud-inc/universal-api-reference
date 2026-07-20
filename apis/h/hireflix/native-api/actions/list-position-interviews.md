# List Position Interviews with Hireflix

Retrieves interviews for a position in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [List Position Interviews](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix position ID. |
| `variables.limit` | body | `number` | yes | The number of interviews to return per page. |
| `variables.direction` | body | `string` | yes | The pagination direction. Use FORWARD for the next page or BACKWARD for the previous page. |
| `variables.lastCursor` | body | `string` | no | The pagination cursor from the previous result page. |
| `variables.filterId` | body | `string` | no | Filter interviews by interview ID. |
| `variables.filterEmail` | body | `string` | no | Filter interviews by candidate email. |
| `variables.filterFirstName` | body | `string` | no | Filter interviews by candidate first name. |
| `variables.filterLastName` | body | `string` | no | Filter interviews by candidate last name. |
| `variables.filterStatus` | body | `string` | no | Filter interviews by Hireflix status. |
