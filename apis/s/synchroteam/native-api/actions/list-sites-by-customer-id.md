# List Sites by Customer ID with Synchroteam

Retrieves sites from Synchroteam for a specific customer ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Site/List/byCustomer/id/:paramValue`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [List Sites by Customer ID](https://api.synchroteam.com/v2/#get-sites-list-by-customer-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paramValue` | path | `string` | yes | Customer id to list sites for. |
