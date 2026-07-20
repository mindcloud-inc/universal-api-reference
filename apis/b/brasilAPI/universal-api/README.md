# <img src="https://images.mindcloud.co/apps/icons/brasilapi-icon_1775846710847.png" alt="Brasil API logo" width="28" height="28"> Brasil API: Universal API

Brasil API provides fast public access to Brazilian reference data such as CEP, CNPJ, banks, holidays, FIPE pricing, IBGE data, PIX participants, CPTEC weather, and related lookup datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brasilAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://brasilapi.com.br
- **Vendor API docs:** https://brasilapi.com.br/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Banks](actions/list-banks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-banks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Get Address by CEP](actions/get-address-by-cep.md) | GET | Retrieves an address from Brasil API by CEP. |
| [Get Address by CEP V2](actions/get-address-by-cep-v2.md) | GET | Retrieves an address and geolocation from Brasil API by CEP. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Airport Weather Conditions](actions/get-airport-weather-conditions.md) | GET | Retrieves current airport weather conditions from Brasil API by ICAO code. |
| [Get Bank](actions/get-bank.md) | GET | Retrieves a bank from Brasil API by code. |
| [Get Book by ISBN](actions/get-book-by-isbn.md) | GET | Retrieves book details from Brasil API by ISBN. |
| [Get Brokerage by CNPJ](actions/get-brokerage-by-cnpj.md) | GET | Retrieves a brokerage from Brasil API by CNPJ. |
| [Get City Weather Forecast](actions/get-city-weather-forecast.md) | GET | Retrieves a one-day city weather forecast from Brasil API. |
| [Get City Weather Forecast by Days](actions/get-city-weather-forecast-by-days.md) | GET | Retrieves a city weather forecast from Brasil API for up to six days. |
| [Get Company by CNPJ](actions/get-company-by-cnpj.md) | GET | Retrieves company details from Brasil API by CNPJ. |
| [Get DDD Info](actions/get-ddd-info.md) | GET | Retrieves DDD cities and state information from Brasil API. |
| [Get Domain Status](actions/get-domain-status.md) | GET | Retrieves a .br domain status from Brasil API. |
| [Get Exchange Rate](actions/get-exchange-rate.md) | GET | Retrieves a BRL exchange rate from Brasil API by currency and date. |
| [Get FIPE Vehicle Prices](actions/get-fipe-vehicle-prices.md) | GET | Retrieves FIPE vehicle prices from Brasil API by FIPE code. |
| [Get IBGE State](actions/get-ibge-state.md) | GET | Retrieves an IBGE state from Brasil API by code. |
| [Get Interest Rate](actions/get-interest-rate.md) | GET | Retrieves an interest rate from Brasil API by symbol. |
| [Get NCM Code](actions/get-ncm-code.md) | GET | Retrieves an NCM code from Brasil API by code. |
| [Get Ocean Forecast](actions/get-ocean-forecast.md) | GET | Retrieves a one-day ocean forecast from Brasil API. |
| [Get Ocean Forecast by Days](actions/get-ocean-forecast-by-days.md) | GET | Retrieves an ocean forecast from Brasil API for up to six days. |
| [List Banks](actions/list-banks.md) | GET | Retrieves Brazilian banks from Brasil API. |
| [List Brokerages](actions/list-brokerages.md) | GET | Retrieves CVM brokerages from Brasil API. |
| [List Capital Weather Conditions](actions/list-capital-weather-conditions.md) | GET | Retrieves current capital weather conditions from Brasil API. |
| [List CPTEC Cities](actions/list-cptec-cities.md) | GET | Retrieves CPTEC cities from Brasil API. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves available currencies from Brasil API. |
| [List FIPE Brands](actions/list-fipe-brands.md) | GET | Retrieves FIPE brands from Brasil API by vehicle type. |
| [List FIPE Reference Tables](actions/list-fipe-reference-tables.md) | GET | Retrieves FIPE reference tables from Brasil API. |
| [List FIPE Vehicles](actions/list-fipe-vehicles.md) | GET | Retrieves FIPE vehicles from Brasil API by brand and vehicle type. |
| [List IBGE Municipalities](actions/list-ibge-municipalities.md) | GET | Retrieves IBGE municipalities from Brasil API by state abbreviation. |
| [List IBGE States](actions/list-ibge-states.md) | GET | Retrieves IBGE states from Brasil API. |
| [List Interest Rates](actions/list-interest-rates.md) | GET | Retrieves Brazilian interest rates from Brasil API. |
| [List National Holidays](actions/list-national-holidays.md) | GET | Retrieves Brazilian national holidays from Brasil API by year. |
| [List NCM Codes](actions/list-ncm-codes.md) | GET | Retrieves NCM codes from Brasil API. |
| [List PIX Participants](actions/list-pix-participants.md) | GET | Retrieves PIX participants from Brasil API. |
| [Search CPTEC Cities](actions/search-cptec-cities.md) | GET | Finds CPTEC cities in Brasil API by city name. |
| [Search NCM Codes](actions/search-ncm-codes.md) | GET | Finds NCM codes in Brasil API by search term. |

