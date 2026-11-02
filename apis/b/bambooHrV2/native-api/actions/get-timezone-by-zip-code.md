# Get Timezone by ZIP Code with BambooHR

Retrieves timezone by zip code from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/timezones/by-zip/:zip`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Timezone by ZIP Code](https://documentation.bamboohr.com/reference/10d66d8561dd7dac50ff9c21ef63d83b)

## Requirements

- **OAuth scopes:** `meta`
- **scope:** `meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | path | `string` | yes | A 5-digit US ZIP code. |
