# List Clients with Quilia

## Endpoint

- **Method:** `GET`
- **Path:** `clients`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [List Clients](https://api.quilia.dev/v2#tag/clients/GET/clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated list of additional fields to include. Available: address_1, address_2, city, state, postal_code, country, date_of_birth, language, timezone |
| `filter[email]` | query | `string` | no | Filter by email. See endpoint description for syntax. |
| `filter[name_first]` | query | `string` | no | Filter by name_first. See endpoint description for syntax. |
| `filter[name_last]` | query | `string` | no | Filter by name_last. See endpoint description for syntax. |
| `filter[name]` | query | `string` | no | Filter by name. See endpoint description for syntax. |
| `filter[phone]` | query | `string` | no | Filter by phone. See endpoint description for syntax. |
