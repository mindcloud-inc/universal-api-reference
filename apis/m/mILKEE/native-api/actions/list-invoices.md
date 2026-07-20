# List Invoices with MILKEE

Retrieves invoices from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/invoices`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Invoices](https://apidocs.milkee.ch/api/resources/invoices.html#alle-rechnungen-auflisten)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
