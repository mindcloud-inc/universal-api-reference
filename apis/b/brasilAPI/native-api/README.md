# Brasil API: Native API Reference

A consolidated summary of Brasil API's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://brasilapi.com.br/docs
- **OpenAPI specification:** https://brasilapi.com.br/docs
- **API base URL:** `https://brasilapi.com.br/api`

## Authentication

### No Authentication

Brasil API is a public API for the documented endpoints used in this app; no credential is required for standard lookup requests.

This API does not require request authentication.

[Official authentication documentation](https://brasilapi.com.br/docs)

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Address by CEP](actions/get-address-by-cep.md) | `GET /cep/v1/{cep}` | [docs](https://brasilapi.com.br/docs) |
| [Get Address by CEP V2](actions/get-address-by-cep-v2.md) | `GET /cep/v2/{cep}` | [docs](https://brasilapi.com.br/docs) |
| [Get Airport Weather Conditions](actions/get-airport-weather-conditions.md) | `GET /cptec/v1/clima/aeroporto/{icaoCode}` | [docs](https://brasilapi.com.br/docs) |
| [Get Bank](actions/get-bank.md) | `GET /banks/v1/{code}` | [docs](https://brasilapi.com.br/docs) |
| [Get Book by ISBN](actions/get-book-by-isbn.md) | `GET /isbn/v1/{isbn}` | [docs](https://brasilapi.com.br/docs) |
| [Get Brokerage by CNPJ](actions/get-brokerage-by-cnpj.md) | `GET /cvm/corretoras/v1/{cnpj}` | [docs](https://brasilapi.com.br/docs) |
| [Get City Weather Forecast](actions/get-city-weather-forecast.md) | `GET /cptec/v1/clima/previsao/{cityCode}` | [docs](https://brasilapi.com.br/docs) |
| [Get City Weather Forecast by Days](actions/get-city-weather-forecast-by-days.md) | `GET /cptec/v1/clima/previsao/{cityCode}/{days}` | [docs](https://brasilapi.com.br/docs) |
| [Get Company by CNPJ](actions/get-company-by-cnpj.md) | `GET /cnpj/v1/{cnpj}` | [docs](https://brasilapi.com.br/docs) |
| [Get DDD Info](actions/get-ddd-info.md) | `GET /ddd/v1/{ddd}` | [docs](https://brasilapi.com.br/docs) |
| [Get Domain Status](actions/get-domain-status.md) | `GET /registrobr/v1/{domain}` | [docs](https://brasilapi.com.br/docs) |
| [Get Exchange Rate](actions/get-exchange-rate.md) | `GET /cambio/v1/cotacao/{moeda}/{data}` | [docs](https://brasilapi.com.br/docs) |
| [Get FIPE Vehicle Prices](actions/get-fipe-vehicle-prices.md) | `GET /fipe/preco/v1/{codigoFipe}` | [docs](https://brasilapi.com.br/docs) |
| [Get IBGE State](actions/get-ibge-state.md) | `GET /ibge/uf/v1/{code}` | [docs](https://brasilapi.com.br/docs) |
| [Get Interest Rate](actions/get-interest-rate.md) | `GET /taxas/v1/{sigla}` | [docs](https://brasilapi.com.br/docs) |
| [Get NCM Code](actions/get-ncm-code.md) | `GET /ncm/v1/{code}` | [docs](https://brasilapi.com.br/docs) |
| [Get Ocean Forecast](actions/get-ocean-forecast.md) | `GET /cptec/v1/ondas/{cityCode}` | [docs](https://brasilapi.com.br/docs) |
| [Get Ocean Forecast by Days](actions/get-ocean-forecast-by-days.md) | `GET /cptec/v1/ondas/{cityCode}/{days}` | [docs](https://brasilapi.com.br/docs) |
| [List Banks](actions/list-banks.md) | `GET /banks/v1` | [docs](https://brasilapi.com.br/docs) |
| [List Brokerages](actions/list-brokerages.md) | `GET /cvm/corretoras/v1` | [docs](https://brasilapi.com.br/docs) |
| [List Capital Weather Conditions](actions/list-capital-weather-conditions.md) | `GET /cptec/v1/clima/capital` | [docs](https://brasilapi.com.br/docs) |
| [List CPTEC Cities](actions/list-cptec-cities.md) | `GET /cptec/v1/cidade` | [docs](https://brasilapi.com.br/docs) |
| [List Currencies](actions/list-currencies.md) | `GET /cambio/v1/moedas` | [docs](https://brasilapi.com.br/docs) |
| [List FIPE Brands](actions/list-fipe-brands.md) | `GET /fipe/marcas/v1/{tipoVeiculo}` | [docs](https://brasilapi.com.br/docs) |
| [List FIPE Reference Tables](actions/list-fipe-reference-tables.md) | `GET /fipe/tabelas/v1` | [docs](https://brasilapi.com.br/docs) |
| [List FIPE Vehicles](actions/list-fipe-vehicles.md) | `GET /fipe/veiculos/v1/{tipoVeiculo}/{codigoMarca}` | [docs](https://brasilapi.com.br/docs) |
| [List IBGE Municipalities](actions/list-ibge-municipalities.md) | `GET /ibge/municipios/v1/{siglaUF}` | [docs](https://brasilapi.com.br/docs) |
| [List IBGE States](actions/list-ibge-states.md) | `GET /ibge/uf/v1` | [docs](https://brasilapi.com.br/docs) |
| [List Interest Rates](actions/list-interest-rates.md) | `GET /taxas/v1` | [docs](https://brasilapi.com.br/docs) |
| [List National Holidays](actions/list-national-holidays.md) | `GET /feriados/v1/{ano}` | [docs](https://brasilapi.com.br/docs) |
| [List NCM Codes](actions/list-ncm-codes.md) | `GET /ncm/v1` | [docs](https://brasilapi.com.br/docs) |
| [List PIX Participants](actions/list-pix-participants.md) | `GET /pix/v1/participants` | [docs](https://brasilapi.com.br/docs) |
| [Search CPTEC Cities](actions/search-cptec-cities.md) | `GET /cptec/v1/cidade/{cityName}` | [docs](https://brasilapi.com.br/docs) |
| [Search NCM Codes](actions/search-ncm-codes.md) | `GET /ncm/v1` | [docs](https://brasilapi.com.br/docs) |
