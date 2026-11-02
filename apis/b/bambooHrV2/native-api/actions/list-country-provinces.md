# List Country Provinces with BambooHR

Lists country provinces from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/provinces/:countryId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Country Provinces](https://documentation.bamboohr.com/reference/get-states-by-country-id)

## Requirements

- **OAuth scopes:** `field`
- **scope:** `field` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryId` | path | `number` | yes | Numeric id of the country, taken from the countries options list. Use the `id` of the target country from `GET /api/v1/meta/countries/options`. |
