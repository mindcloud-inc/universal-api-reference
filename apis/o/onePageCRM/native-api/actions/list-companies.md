# List Companies with OnePageCRM

Retrieves companies from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Companies](https://developer.onepagecrm.com/api/#/Companies/get_companies)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Search companies by name |
| `phone` | query | `string` | no | Search companies by phone number |
| `letter` | query | `string` | no | Return companies whose name begins with the specified letter |
