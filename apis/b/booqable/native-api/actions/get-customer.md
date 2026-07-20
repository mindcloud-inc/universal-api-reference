# Get Customer with Booqable

Retrieves a customer from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Customer](https://developers.booqable.com/#customers-fetch-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Customer ID. |
| `fields[customers]` | query | `string` | no | Comma-separated customer fields to include instead of the default field set. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
