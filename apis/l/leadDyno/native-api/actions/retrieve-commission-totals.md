# Retrieve Commission Totals with LeadDyno

Retrieves commission totals from your LeadDyno account.

## Endpoint

- **Method:** `GET`
- **Path:** `/commissions/totals`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Retrieve Commission Totals](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/get-commissions-totals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `number` | no | The affiliate ID whose commissions are to be retrieved. |
| `currency` | query | `string` | no | The commission currency code. |
