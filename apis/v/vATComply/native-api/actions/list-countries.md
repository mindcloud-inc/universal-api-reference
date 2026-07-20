# List Countries with VAT Comply

Retrieves a list of countries from VAT Comply.

## Endpoint

- **Method:** `GET`
- **Path:** `/countries`
- **Base URL:** `https://api.vatcomply.com`
- **Official documentation:** [List Countries](https://www.vatcomply.com/api/countries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Filter countries by a search string. |
| `region` | query | `string` | no | Filter countries by region. |
| `subregion` | query | `string` | no | Filter countries by subregion. |
| `currency` | query | `string` | no | Filter countries by currency code. |
