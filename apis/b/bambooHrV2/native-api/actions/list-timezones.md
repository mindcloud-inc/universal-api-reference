# List Timezones with BambooHR

Lists timezones from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/timezones`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Timezones](https://documentation.bamboohr.com/reference/5c5fb0f1211ae1c9451753f92f1053b6)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Ordering by OData (Open Data Protocol) v4 specification |
| `select` | query | `string` | no | Projection (field selection) by OData specification |
| `filter` | query | `string` | no | Filter by an OData (Open Data Protocol) v4 specification |
