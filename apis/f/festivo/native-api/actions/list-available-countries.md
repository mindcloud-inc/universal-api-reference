# List Available Countries with Festivo

Retrieves available country codes from Festivo.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-holidays/countries`
- **Base URL:** `https://api.getfestivo.com/v3`
- **Official documentation:** [List Available Countries](https://docs.getfestivo.com/docs/products/public-holidays-api/list-countries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `string` | no | Optional ISO 3166-1 alpha-2 country code filter, for example US. |
