# List Call Centers with Dialpad

## Endpoint

- **Method:** `GET`
- **Path:** `/callcenters`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Call Centers](https://developers.dialpad.com/reference/callcenterslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `office_id` | query | `number` | no | Filter call centers by Dialpad office ID. |
| `name_search` | query | `string` | no | Filter call centers by name substring. |
| `cursor` | query | `string` | no | Pagination cursor from a previous Dialpad call centers response. |
