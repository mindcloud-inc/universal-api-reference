# Read Credit History with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/account/readcredithistory`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Read Credit History](https://www.smsgatewaycenter.com/developer-api/read-credit-history/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromdate` | body | `string` | yes | Start date for the credit-history window as a literal provider date string, for example 2026-04-01. |
| `todate` | body | `string` | yes | End date for the credit-history window as a literal provider date string, for example 2026-04-03. |
