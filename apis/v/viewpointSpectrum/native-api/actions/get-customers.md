# Get Customers with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/GetCustomers`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Get Customers](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyCode` | body | `string` | no |
| `customerCode` | body | `string` | no |
| `pStatus` | body | `list` | no |
