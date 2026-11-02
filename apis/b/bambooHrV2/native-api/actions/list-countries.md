# List Countries with BambooHR

Lists countries from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/countries/options`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Countries](https://documentation.bamboohr.com/reference/get-countries-options)

## Requirements

- **OAuth scopes:** `field meta`
- **scope:** `field, meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isoCode` | query | `string` | no | ISO 3166-1 alpha-2 country code (exactly two letters). When present, returns the matching country as a single object instead of the full array. Maximum length: 2. |
