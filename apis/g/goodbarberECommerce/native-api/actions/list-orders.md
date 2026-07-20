# List Orders with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/orders/:webzine_id/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Orders](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creation_date_from` | query | `string` | no | Restricts the list of returned orders to the ones created after (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. |
| `creation_date_to` | query | `string` | no | Restricts the list of returned orders to the ones created before (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. |
| `delivery_date_from` | query | `string` | no | Restricts the list of returned orders to the ones whose selected delivery slot lands after (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. When this filter is applied, orders that do not have a selected delivery slot (shipped by transporter, for instance) will not be returned. Also, note that a delivery slot is said to land after a given datetime if its slot_start value is later than that datetime. |
| `delivery_date_to` | query | `string` | no | Restricts the list of returned orders to the ones whose selected delivery slot lands before (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. When this filter is applied, orders that do not have a selected delivery slot (shipped by transporter, for instance) will not be returned. Also, note that a delivery slot is said to land before a given datetime if its slot_end value comes before that datetime. |
| `status` | query | `string` | no | Restricts the list of returned orders to a certain status. To filter several statuses use the following syntax: ?status={STATUS1}&status={STATUS2} |
