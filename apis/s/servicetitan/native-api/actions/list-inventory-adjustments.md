# List Inventory Adjustments with ServiceTitan

Retrieves inventory adjustments from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `inventory/v2/tenant/{tenant}/adjustments`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Inventory Adjustments](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Adjustments_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | Return items modified on or after certain date/time (in UTC) |
| `sort` | query | `string` | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order.  Available fields are: Id, ModifiedOn, CreatedOn. |
| `syncStatuses` | query | `string` | no | Filter by a collection of sync statues |
