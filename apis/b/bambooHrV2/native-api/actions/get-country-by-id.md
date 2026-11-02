# Get Country by ID with BambooHR

Retrieves country by id from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/countries/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Country by ID](https://documentation.bamboohr.com/reference/get-country-by-id)

## Requirements

- **OAuth scopes:** `meta`
- **scope:** `meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Country id, as a numeric string. Obtain valid ids from the `id` field of Get Countries (`get-countries-options`). |
