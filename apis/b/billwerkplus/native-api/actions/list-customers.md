# List Customers with Billwerkplus

Retrieves customers from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/customer`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Customers](https://docs.frisbii.com/reference/getcustomerlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | query | `string` | no | Filter by exact customer handle. |
| `email` | query | `string` | no | Filter by customer email. |
