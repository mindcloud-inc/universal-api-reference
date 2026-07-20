# Get Quote by ID with IRIS KashFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/service.asmx`
- **Base URL:** `https://securedwebapp.com`
- **Official documentation:** [Get Quote by ID](https://www.kashflow.com/developers/soap-api/getquotebyid/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `QuoteID` | body | `number` | yes |
