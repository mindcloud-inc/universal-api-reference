# REST Countries: Native API Reference

A consolidated summary of REST Countries's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://restcountries.com/
- **API base URL:** `https://restcountries.com/v3.1`

## Authentication

### No authentication

REST Countries is a public API and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://restcountries.com/)

## API conventions

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Country by Code](actions/get-country-by-code.md) | `GET alpha/:code` | [docs](https://restcountries.com/) |
| [Get Country by Full Name](actions/get-country-by-full-name.md) | `GET name/:name` | [docs](https://restcountries.com/) |
| [Get Country Currencies by Code](actions/get-country-currencies-by-code.md) | `GET alpha/:code?fields=name,currencies` | [docs](https://restcountries.com/) |
| [Get Country Languages by Code](actions/get-country-languages-by-code.md) | `GET alpha/:code?fields=name,languages` | [docs](https://restcountries.com/) |
| [Get Country Population by Code](actions/get-country-population-by-code.md) | `GET alpha/:code?fields=name,population,region,subregion` | [docs](https://restcountries.com/) |
| [List All Countries](actions/list-all-countries.md) | `GET all?fields=name,cca2,cca3,region,subregion,capital,population,independent,unMember,flags` | [docs](https://restcountries.com/) |
| [List Countries by Region](actions/list-countries-by-region.md) | `GET region/:region` | [docs](https://restcountries.com/) |
| [List Countries by Subregion](actions/list-countries-by-subregion.md) | `GET subregion/:subregion` | [docs](https://restcountries.com/) |
| [List Country Areas](actions/list-country-areas.md) | `GET all?fields=name,area,region,subregion` | [docs](https://restcountries.com/) |
| [List Country Borders](actions/list-country-borders.md) | `GET all?fields=name,borders,cca3` | [docs](https://restcountries.com/) |
| [List Country Calling Codes](actions/list-country-calling-codes.md) | `GET all?fields=name,idd` | [docs](https://restcountries.com/) |
| [List Country Car Side Rules](actions/list-country-car-side-rules.md) | `GET all?fields=name,car` | [docs](https://restcountries.com/) |
| [List Country Continents](actions/list-country-continents.md) | `GET all?fields=name,continents,region,subregion` | [docs](https://restcountries.com/) |
| [List Country Currencies](actions/list-country-currencies.md) | `GET all?fields=name,currencies` | [docs](https://restcountries.com/) |
| [List Country Languages](actions/list-country-languages.md) | `GET all?fields=name,languages` | [docs](https://restcountries.com/) |
| [List Country Maps](actions/list-country-maps.md) | `GET all?fields=name,maps` | [docs](https://restcountries.com/) |
| [List Country Names and Capitals](actions/list-country-names-and-capitals.md) | `GET all?fields=name,capital,region,subregion` | [docs](https://restcountries.com/) |
| [List Country Names and Codes](actions/list-country-names-and-codes.md) | `GET all?fields=name,cca2,cca3,ccn3` | [docs](https://restcountries.com/) |
| [List Country Names and Flags](actions/list-country-names-and-flags.md) | `GET all?fields=name,flags,cca2,cca3` | [docs](https://restcountries.com/) |
| [List Country Populations](actions/list-country-populations.md) | `GET all?fields=name,population,region` | [docs](https://restcountries.com/) |
| [List Country Start of Week](actions/list-country-start-of-week.md) | `GET all?fields=name,startOfWeek` | [docs](https://restcountries.com/) |
| [List Country Timezones](actions/list-country-timezones.md) | `GET all?fields=name,timezones` | [docs](https://restcountries.com/) |
| [List Country Top Level Domains](actions/list-country-top-level-domains.md) | `GET all?fields=name,tld` | [docs](https://restcountries.com/) |
| [List Independent Countries](actions/list-independent-countries.md) | `GET independent` | [docs](https://restcountries.com/) |
| [Search Countries by Capital](actions/search-countries-by-capital.md) | `GET capital/:capital` | [docs](https://restcountries.com/) |
| [Search Countries by Currency](actions/search-countries-by-currency.md) | `GET currency/:currency` | [docs](https://restcountries.com/) |
| [Search Countries by Demonym](actions/search-countries-by-demonym.md) | `GET demonym/:demonym` | [docs](https://restcountries.com/) |
| [Search Countries by Language](actions/search-countries-by-language.md) | `GET lang/:language` | [docs](https://restcountries.com/) |
| [Search Countries by Name](actions/search-countries-by-name.md) | `GET name/:name` | [docs](https://restcountries.com/) |
| [Search Countries by Translation](actions/search-countries-by-translation.md) | `GET translation/:translation` | [docs](https://restcountries.com/) |
