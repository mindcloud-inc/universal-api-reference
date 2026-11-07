# List Customers with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/GetCustomers`
- **Base URL:** `{url}:8482/`
- **API:** REST
- **Official documentation:** [List Customers](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/get-customers)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pStatus` | body | `list` | no | Accepted values: `ALL`, `I`. |
