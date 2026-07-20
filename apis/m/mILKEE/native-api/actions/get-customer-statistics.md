# Get Customer Statistics with MILKEE

Retrieves customer statistics from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/customers/:customerId/statistics`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Customer Statistics](https://apidocs.milkee.ch/api/resources/customers.html#kundenstatistiken-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer` | path | `string` | yes | The numeric MILKEE customer ID used in the request path. |
