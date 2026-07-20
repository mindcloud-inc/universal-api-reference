# Get Materials with ServiceTitan

Retrieves pricebook materials from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `pricebook/v2/tenant/{tenant}/materials`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Materials](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=Materials_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | Format - date-time (as date-time in RFC3339). Return items created on or after certain date/time (in UTC) |
| `sort` | query | `string` | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order.  Available fields are: Id, Code, DisplayName, CreatedOn, ModifiedOn, Price, MemberPrice, AddOnPrice, AddOnMemberPrice, MaterialsCost, PrimaryVendor, Cost, Manufacturer, Priority. |
