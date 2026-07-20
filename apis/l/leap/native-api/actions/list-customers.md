# List Customers with Leap

Retrieves customer records from Leap.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [List Customers](https://docs.api.jobprogress.com/api/customer.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of items to return, up to 100. |
| `page` | query | `number` | no | Page number for pagination. |
| `query` | query | `string` | no | Search customers by email and full name. |
