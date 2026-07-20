# View all the available numbers with filters with Routee

Retrieves all the available numbers with filters from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/available/search`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View all the available numbers with filters](https://docs.routee.net/reference/view-all-the-available-numbers-with-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `fieldName` | body | `string` | yes | The name of the field to filter. Available values are: **country** (required), **msisdn**, **service**, **areaCode** *(Works for the countries US and Canada only)* and **type** ("VLN" or "TOLL_FREE", *Works for the countries US and Canada only).* |
| `searchTerm` | body | `string` | yes | The exact value that the specified field must match. |
| `searchOperator` | body | `string` | no | Optional: The operator upon which the search operation will be executed. Possible values: 'is', 'contains', 'starts_with', 'ends_with'. If missing defaults to 'is'. |
