# List Categories with Walmart

Retrieve a list of categories for a specific department.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/utilities/taxonomy/departments/:departmentId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Categories](https://developer.walmart.com/us-marketplace/reference/getcategories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | A `departmentId` to retrieve categories for. |
