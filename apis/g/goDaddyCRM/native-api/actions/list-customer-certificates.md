# List Customer Certificates with GoDaddy CRM

Retrieves certificates for a GoDaddy customer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/certificates`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [List Customer Certificates](https://developer.godaddy.com/doc/endpoint/certificates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier whose certificates should be listed |
