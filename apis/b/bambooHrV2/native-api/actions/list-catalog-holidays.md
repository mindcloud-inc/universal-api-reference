# List Catalog Holidays with BambooHR

Lists catalog holidays from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/holidays/catalog`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Catalog Holidays](https://documentation.bamboohr.com/reference/list-catalog-holidays)

## Requirements

- **OAuth scopes:** `holidays`
- **scope:** `holidays` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | query | `string` | no | ISO 3166-1 alpha-2 country code. Filters the catalog to entries for the given country. |
| `year` | query | `number` | no | Calendar year. Filters the catalog to entries whose startDate falls in the given year. |
| `filter` | query | `string` | no | OData v4 filter expression. Supported fields: name, type, countryCode, startDate. Example: startDate ge '2026-01-01' and type eq 'PUBLIC' |
| `orderBy` | query | `string` | no | Sort expression. Allowed fields: startDate, name, with optional asc/desc direction. |
