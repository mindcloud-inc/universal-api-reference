# Směnné kurzy ČNB: Native API Reference

A consolidated summary of Směnné kurzy ČNB's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.cnb.cz/cnbapi/swagger-ui.html
- **OpenAPI specification:** https://api.cnb.cz/cnbapi/api-docs
- **API base URL:** `https://api.cnb.cz/cnbapi`

## Authentication

### No auth

Public CNB API with no credentials

This API does not require request authentication.

[Official authentication documentation](https://www.cnb.cz/cs/casto-kladene-dotazy/Kurzy-devizoveho-trhu-na-www-strankach-CNB/)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get CNB Czeonia Daily](actions/get-cnb-czeonia-daily.md) | `GET /czeonia/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Czeonia Daily by Year](actions/get-cnb-czeonia-daily-by-year.md) | `GET /czeonia/daily-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Daily Exchange Rates](actions/get-cnb-daily-exchange-rates.md) | `GET /exrates/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Daily Exchange Rates by Currency and Month](actions/get-cnb-daily-exchange-rates-by-currency-and-month.md) | `GET /exrates/daily-currency-month` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Daily Exchange Rates by Year](actions/get-cnb-daily-exchange-rates-by-year.md) | `GET /exrates/daily-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Forward Daily](actions/get-cnb-forward-daily.md) | `GET /forward/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Forward Daily by Currency Pair, Date Range, and Maturity](actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity.md) | `GET /forward/daily-range-currency-pair-maturity` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Monthly Average Exchange Rates by Currency](actions/get-cnb-monthly-average-exchange-rates-by-currency.md) | `GET /exrates/monthly-averages-currency` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Monthly Average Exchange Rates by Year](actions/get-cnb-monthly-average-exchange-rates-by-year.md) | `GET /exrates/monthly-averages-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Monthly Cumulative Average Exchange Rates by Currency](actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency.md) | `GET /exrates/monthly-cumulative-averages-currency` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Monthly Cumulative Average Exchange Rates by Year](actions/get-cnb-monthly-cumulative-average-exchange-rates-by-year.md) | `GET /exrates/monthly-cumulative-averages-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB PRIBOR Daily](actions/get-cnb-pribor-daily.md) | `GET /pribor/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB PRIBOR Daily by Year](actions/get-cnb-pribor-daily-by-year.md) | `GET /pribor/daily-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB PRIBOR Daily by Year and Term](actions/get-cnb-pribor-daily-by-year-and-term.md) | `GET /pribor/daily-year-term` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Quarterly Average Exchange Rates by Currency](actions/get-cnb-quarterly-average-exchange-rates-by-currency.md) | `GET /exrates/quarterly-averages-currency` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB Quarterly Average Exchange Rates by Year](actions/get-cnb-quarterly-average-exchange-rates-by-year.md) | `GET /exrates/quarterly-averages-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB FX Rates by Currency and Month Range](actions/get-cnbfx-rates-by-currency-and-month-range.md) | `GET /fxrates/daily-range-currency` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB FX Rates by Month](actions/get-cnbfx-rates-by-month.md) | `GET /fxrates/daily-month` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB FX Rates by Year](actions/get-cnbfx-rates-by-year.md) | `GET /fxrates/daily-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB OMO Daily](actions/get-cnbomo-daily.md) | `GET /omo/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB OMO Daily by Year](actions/get-cnbomo-daily-by-year.md) | `GET /omo/daily-year` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
| [Get CNB SKD Daily](actions/get-cnbskd-daily.md) | `GET /skd/daily` | [docs](https://api.cnb.cz/cnbapi/swagger-ui.html) |
