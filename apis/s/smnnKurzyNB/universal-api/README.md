# <img src="https://images.mindcloud.co/apps/icons/smnn-kurzy-nb-icon_1782394509902.png" alt="Směnné kurzy ČNB logo" width="28" height="28"> Směnné kurzy ČNB: Universal API

Browse CNB exchange rates and averages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smnnKurzyNB/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cnb.cz/
- **Vendor API docs:** https://api.cnb.cz/cnbapi/swagger-ui.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get CNB Czeonia Daily](actions/get-cnb-czeonia-daily.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get CNB Czeonia Daily](actions/get-cnb-czeonia-daily.md) | GET | Retrieves the last valid CZEONIA rate from Směnné kurzy ČNB. |
| [Get CNB Czeonia Daily by Year](actions/get-cnb-czeonia-daily-by-year.md) | GET | Retrieves CZEONIA rates for a year from Směnné kurzy ČNB. |
| [Get CNB Daily Exchange Rates](actions/get-cnb-daily-exchange-rates.md) | GET | Retrieves the last valid daily exchange rates from Směnné kurzy ČNB. |
| [Get CNB Daily Exchange Rates by Currency and Month](actions/get-cnb-daily-exchange-rates-by-currency-and-month.md) | GET | Retrieves daily exchange rates for a currency and month from Směnné kurzy ČNB. |
| [Get CNB Daily Exchange Rates by Year](actions/get-cnb-daily-exchange-rates-by-year.md) | GET | Retrieves daily exchange rates for a year from Směnné kurzy ČNB. |
| [Get CNB Forward Daily](actions/get-cnb-forward-daily.md) | GET | Retrieves the last valid forward rates from Směnné kurzy ČNB. |
| [Get CNB Forward Daily by Currency Pair, Date Range, and Maturity](actions/get-cnb-forward-daily-by-currency-pair-date-range-and-maturity.md) | GET | Retrieves forward rates by currency pair, date range, and maturity from Směnné kurzy ČNB. |
| [Get CNB Monthly Average Exchange Rates by Currency](actions/get-cnb-monthly-average-exchange-rates-by-currency.md) | GET | Retrieves monthly average exchange rates for a currency from Směnné kurzy ČNB. |
| [Get CNB Monthly Average Exchange Rates by Year](actions/get-cnb-monthly-average-exchange-rates-by-year.md) | GET | Retrieves monthly average exchange rates for a year from Směnné kurzy ČNB. |
| [Get CNB Monthly Cumulative Average Exchange Rates by Currency](actions/get-cnb-monthly-cumulative-average-exchange-rates-by-currency.md) | GET | Retrieves monthly cumulative average exchange rates for a currency from Směnné kurzy ČNB. |
| [Get CNB Monthly Cumulative Average Exchange Rates by Year](actions/get-cnb-monthly-cumulative-average-exchange-rates-by-year.md) | GET | Retrieves monthly cumulative average exchange rates for a year from Směnné kurzy ČNB. |
| [Get CNB PRIBOR Daily](actions/get-cnb-pribor-daily.md) | GET | Retrieves the last valid PRIBOR data from Směnné kurzy ČNB. |
| [Get CNB PRIBOR Daily by Year](actions/get-cnb-pribor-daily-by-year.md) | GET | Retrieves PRIBOR data for a year from Směnné kurzy ČNB. |
| [Get CNB PRIBOR Daily by Year and Term](actions/get-cnb-pribor-daily-by-year-and-term.md) | GET | Retrieves PRIBOR data for a year and term from Směnné kurzy ČNB. |
| [Get CNB Quarterly Average Exchange Rates by Currency](actions/get-cnb-quarterly-average-exchange-rates-by-currency.md) | GET | Retrieves quarterly average exchange rates for a currency from Směnné kurzy ČNB. |
| [Get CNB Quarterly Average Exchange Rates by Year](actions/get-cnb-quarterly-average-exchange-rates-by-year.md) | GET | Retrieves quarterly average exchange rates for a year from Směnné kurzy ČNB. |
| [Get CNB FX Rates by Currency and Month Range](actions/get-cnbfx-rates-by-currency-and-month-range.md) | GET | Retrieves daily FX rates for a currency and month range from Směnné kurzy ČNB. |
| [Get CNB FX Rates by Month](actions/get-cnbfx-rates-by-month.md) | GET | Retrieves daily FX rates for a month from Směnné kurzy ČNB. |
| [Get CNB FX Rates by Year](actions/get-cnbfx-rates-by-year.md) | GET | Retrieves daily FX rates for a year from Směnné kurzy ČNB. |
| [Get CNB OMO Daily](actions/get-cnbomo-daily.md) | GET | Retrieves the last valid OMO data from Směnné kurzy ČNB. |
| [Get CNB OMO Daily by Year](actions/get-cnbomo-daily-by-year.md) | GET | Retrieves OMO data for a year from Směnné kurzy ČNB. |
| [Get CNB SKD Daily](actions/get-cnbskd-daily.md) | GET | Retrieves the last valid SKD data from Směnné kurzy ČNB. |

