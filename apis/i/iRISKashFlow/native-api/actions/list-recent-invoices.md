# List Recent Invoices with IRIS KashFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/service.asmx`
- **Base URL:** `https://securedwebapp.com`
- **Official documentation:** [List Recent Invoices](https://www.kashflow.com/developers/soap-api/getinvoices-recent/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `NumberOfInvoices` | body | `number` | yes | How many recent invoices to return. |
