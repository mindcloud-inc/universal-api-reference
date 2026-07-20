# Purchase CO2 Removal with CDR Platform

Creates a CO2 removal purchase in CDR Platform.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cdr/`
- **Base URL:** `https://api.cdrplatform.com`
- **Official documentation:** [Purchase CO2 Removal](https://api.cdrplatform.com/schema/redoc/#tag/CO2-Removal/operation/cdr_purchase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weight_unit` | body | `list<string>` | yes | Unit for the CO2 removal amount. Accepted values: `g`, `kg`, `t`. |
| `currency` | body | `list<string>` | yes | Currency for the purchase request. Accepted values: `chf`, `eur`, `gbp`, `usd`. |
| `items[].method_type` | body | `list<string>` | yes | Carbon removal method type for an item. Accepted values: `bio-oil`, `forestation`, `kelp-sinking`, `olivine`. |
| `items[].cdr_amount` | body | `number` | yes | Amount of CO2 removal for an item, in the selected weight unit. |
| `client_reference_id` | body | `string` | no | Optional client reference ID to store with the purchase request. Maximum length: 128. |
| `certificate_display_name` | body | `string` | no | Optional display name for the removal certificate. Maximum length: 128. |
