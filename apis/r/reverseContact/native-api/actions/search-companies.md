# Search Companies with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/search/companies`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Search Companies](https://app.reversecontact.com/docs/endpoints/search-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyDomain` | body | `string` | no | Filter by company website domain, such as openai.com. |
| `companyName` | body | `string` | no | Filter by company name. |
