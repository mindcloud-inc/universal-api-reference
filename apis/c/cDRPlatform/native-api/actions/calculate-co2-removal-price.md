# Calculate CO2 Removal Price with CDR Platform

Calculates CO2 removal pricing in CDR Platform.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cdr/price/`
- **Base URL:** `https://api.cdrplatform.com`
- **Official documentation:** [Calculate CO2 Removal Price](https://api.cdrplatform.com/schema/redoc/#tag/CO2-Removal/operation/cdr_price)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weight_unit` | body | `list<string>` | yes | Unit for the CO2 removal amount. Accepted values: `g`, `kg`, `t`. |
| `currency` | body | `list<string>` | yes | Currency for the price calculation. Accepted values: `chf`, `eur`, `gbp`, `usd`. |
| `items[].method_type` | body | `list<string>` | yes | Carbon removal method type for an item. Accepted values: `bio-oil`, `forestation`, `kelp-sinking`, `olivine`. |
| `items[].cdr_amount` | body | `number` | yes | Amount of CO2 removal for an item, in the selected weight unit. |
