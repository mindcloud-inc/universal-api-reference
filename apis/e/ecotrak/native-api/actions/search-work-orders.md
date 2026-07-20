# Search Work Orders with Ecotrak

Finds work orders in Ecotrak by status or updated date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workorders/search`
- **Base URL:** `https://api.ecotrak.com`
- **Official documentation:** [Search Work Orders](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-work-order-search-work-order)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter work orders by status. |
| `updated_date` | query | `string` | no | Filter work orders by updated date. Format YYYY-MM-DD. |
