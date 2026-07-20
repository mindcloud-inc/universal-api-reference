# List Newsletters with Customer.io

Retrieves newsletters from Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/newsletters`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Newsletters](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/listNewsletters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `list<string>` | no | Sort newsletters in chronological asc or reverse chronological desc order. Accepted values: `asc`, `desc`. |
