# <img src="https://images.mindcloud.co/apps/icons/r-estcountries_1776080001966.png" alt="REST Countries logo" width="28" height="28"> REST Countries: Universal API

Public reference API for country, region, language, currency, and geographic metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rESTCountries/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://restcountries.com/
- **Vendor API docs:** https://restcountries.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Country Names and Flags](actions/list-country-names-and-flags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Country by Code](actions/get-country-by-code.md) | GET |  |
| [Get Country by Full Name](actions/get-country-by-full-name.md) | GET |  |
| [Get Country Currencies by Code](actions/get-country-currencies-by-code.md) | GET |  |
| [Get Country Languages by Code](actions/get-country-languages-by-code.md) | GET |  |
| [Get Country Population by Code](actions/get-country-population-by-code.md) | GET |  |
| [List All Countries](actions/list-all-countries.md) | GET |  |
| [List Countries by Region](actions/list-countries-by-region.md) | GET |  |
| [List Countries by Subregion](actions/list-countries-by-subregion.md) | GET |  |
| [List Country Areas](actions/list-country-areas.md) | GET |  |
| [List Country Borders](actions/list-country-borders.md) | GET |  |
| [List Country Calling Codes](actions/list-country-calling-codes.md) | GET |  |
| [List Country Car Side Rules](actions/list-country-car-side-rules.md) | GET |  |
| [List Country Continents](actions/list-country-continents.md) | GET |  |
| [List Country Currencies](actions/list-country-currencies.md) | GET |  |
| [List Country Languages](actions/list-country-languages.md) | GET |  |
| [List Country Maps](actions/list-country-maps.md) | GET |  |
| [List Country Names and Capitals](actions/list-country-names-and-capitals.md) | GET |  |
| [List Country Names and Codes](actions/list-country-names-and-codes.md) | GET |  |
| [List Country Names and Flags](actions/list-country-names-and-flags.md) | GET |  |
| [List Country Populations](actions/list-country-populations.md) | GET |  |
| [List Country Start of Week](actions/list-country-start-of-week.md) | GET |  |
| [List Country Timezones](actions/list-country-timezones.md) | GET |  |
| [List Country Top Level Domains](actions/list-country-top-level-domains.md) | GET |  |
| [List Independent Countries](actions/list-independent-countries.md) | GET |  |
| [Search Countries by Capital](actions/search-countries-by-capital.md) | GET |  |
| [Search Countries by Currency](actions/search-countries-by-currency.md) | GET |  |
| [Search Countries by Demonym](actions/search-countries-by-demonym.md) | GET |  |
| [Search Countries by Language](actions/search-countries-by-language.md) | GET |  |
| [Search Countries by Name](actions/search-countries-by-name.md) | GET |  |
| [Search Countries by Translation](actions/search-countries-by-translation.md) | GET |  |

