# Get Invoice by ID with IRIS KashFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/service.asmx`
- **Base URL:** `https://securedwebapp.com`
- **Official documentation:** [Get Invoice by ID](https://www.kashflow.com/developers/soap-api/getinvoicebyid/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `InvoiceID` | body | `number` | yes |
