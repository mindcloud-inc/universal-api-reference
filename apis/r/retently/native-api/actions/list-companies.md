# List Companies with Retently

Retrieves a list of companies from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/companies`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [List Companies](https://www.retently.com/api/#api-get-companies-get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The current page number. Default 1; |
| `limit` | query | `number` | no | The items limit. Default 20. Maximum 1,000; |
| `sort` | query | `string` | no | Use â-â to pull results in descending order. Example: sort=-companyName |
