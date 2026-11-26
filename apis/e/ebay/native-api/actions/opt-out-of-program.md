# Opt-Out of Program with eBay

This method opts the seller out of an eBay seller program. Refer to the Account API overview for information about available eBay seller programs.

## Endpoint

- **Method:** `POST`
- **Path:** `sell/account/v1/program/opt_out`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Opt-Out of Program](https://developer.ebay.com/api-docs/sell/account/resources/program/methods/optOutOfProgram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programType` | body | `list<string>` | no | The Seller Program to opt-in to. Accepted values: `OUT_OF_STOCK_CONTROL`, `PARTNER_MOTORS_DEALER`, `SELLING_POLICY_MANAGEMENT`. |
