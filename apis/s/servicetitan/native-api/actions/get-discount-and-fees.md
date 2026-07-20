# Get Discount and Fees with ServiceTitan

Retrieves pricebook discounts and fees from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `pricebook/v2/tenant/{tenant}/discounts-and-fees`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Discount and Fees](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=DiscountAndFees_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | Return items modified on or after certain date/time (in UTC) |
| `createdOnOrAfter` | query | `string` | no | Return items created on or after certain date/time (in UTC) |
| `sort` | query | `string` | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order.  Available fields are: Id, Code, DisplayName, CreatedOn, ModifiedOn, Price, MemberPrice, AddOnPrice, AddOnMemberPrice, MaterialsCost, PrimaryVendor, Cost, Manufacturer, Priority. |
