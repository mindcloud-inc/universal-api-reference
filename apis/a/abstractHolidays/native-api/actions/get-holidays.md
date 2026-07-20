# Get Holidays with Abstract Holidays

Retrieves holidays from Abstract Holidays for a country and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/`
- **Base URL:** `https://holidays.abstractapi.com`
- **Official documentation:** [Get Holidays](https://docs.abstractapi.com/api/holidays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code, such as US or SG. Maximum length: 2. |
| `year` | query | `string` | no | Four-digit year to retrieve holidays for. Required for Abstract free-plan connections and for month/day queries; paid plans may support defaulting for broader lookups. |
| `month` | query | `string` | no | Month to retrieve, formatted as 01-12. Required for Abstract free-plan individual-day lookups and whenever Day is provided. |
| `day` | query | `string` | no | Day of month to retrieve, formatted as 01-31. Use with Year and Month for the current verified free-plan lookup path. |
