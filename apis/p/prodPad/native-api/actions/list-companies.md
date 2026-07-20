# List Companies with ProdPad

Retrieves companies from ProdPad.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [List Companies](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetCompanies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Filter companies by ISO Alpha-2 country code. |
| `company_size` | query | `string` | no | Filter companies by company size. |
| `value` | query | `string` | no | Filter companies by value. |
| `city` | query | `string` | no | Filter companies by city. |
| `tags` | query | `string` | no | Filter companies by one or more tag IDs or UUIDs. Send multiple values as a string separated by `,`. |
| `name` | query | `string` | no | Filter companies by company name or partial name. |
| `external_id` | query | `string` | no | Filter companies by an external ID. |
| `external_url` | query | `string` | no | Filter companies by an external URL. |
| `contacts` | query | `boolean` | no | Include contacts associated with each company. |
| `feedbacks` | query | `boolean` | no | Include feedback associated with each company's contacts. |
