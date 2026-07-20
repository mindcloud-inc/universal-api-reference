# List Customer Addresses with Cratejoy

Retrieves a customer's addresses from Cratejoy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customerId/addresses/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [List Customer Addresses](https://docs.cratejoy.com/reference/methods-customer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | The Cratejoy customer ID. |
