# Get Next Invoice Number with MILKEE

Retrieves the next invoice number from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/invoices/number`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Next Invoice Number](https://apidocs.milkee.ch/api/resources/invoices.html#nachste-rechnungsnummer-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
