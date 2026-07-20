# Get Customer with Grand Avenue Software

Retrieves a customer from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Customers/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
