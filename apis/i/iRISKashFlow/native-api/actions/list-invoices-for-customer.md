# List Invoices for Customer with IRIS KashFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/service.asmx`
- **Base URL:** `https://securedwebapp.com`
- **Official documentation:** [List Invoices for Customer](https://www.kashflow.com/developers/soap-api/getinvoicesforcustomer/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CustID` | body | `number` | yes |
