# Delete Employment with Leave Dates

Deletes an existing employment from Leave Dates.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/employments/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Delete Employment](https://api.leavedates.com/documentation#/Employment/delete_employments__id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Employment ID |
| `company_id` | body | `string` | yes | Company ID for the employment |
