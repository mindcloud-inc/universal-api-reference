# List Invoices with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoices`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Invoices](https://docs.fingertip.com/openapi-specs/list-invoices.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | ID of the site to list invoices for. |
| `status` | query | `string` | no | Optional invoice status filter. |
