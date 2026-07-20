# Create Top-Up Invoice with Rye

Creates an on-demand top-up invoice in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/billing/drawdown/topup`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Create Top-Up Invoice](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amountSubunits` | body | `number` | yes | Amount in smallest currency unit. |
| `chargeAutomatically` | body | `boolean` | no | Override whether to automatically charge the invoice. |
