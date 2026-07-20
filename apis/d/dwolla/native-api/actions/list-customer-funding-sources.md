# List Customer Funding Sources with Dwolla

Retrieves funding sources for a Dwolla customer.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/[:id]/funding-sources`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [List Customer Funding Sources](https://developers.dwolla.com/docs/api-reference/funding-sources/list-customer-funding-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla customer ID. |
