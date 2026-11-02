# Get Currency Conversion Rates with BambooHR

Retrieves currency conversion rates from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/currency-conversions`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Currency Conversion Rates](https://documentation.bamboohr.com/reference/get-currency-conversions)

## Requirements

- **OAuth scopes:** `meta`
- **scope:** `meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseCurrency` | query | `string` | no | ISO 4217 alphabetic base currency code (for example USD or EUR). Case-insensitive; values are normalized to uppercase. Defaults to USD when omitted. A well-formed code with no stored rate snapshot returns 404. Maximum length: 3. |
