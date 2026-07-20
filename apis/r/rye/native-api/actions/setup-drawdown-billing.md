# Setup Drawdown Billing with Rye

Updates drawdown billing settings in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/billing/drawdown`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Setup Drawdown Billing](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargeAutomatically` | body | `boolean` | no | Whether to automatically charge the invoice when created. |
| `minBalanceSubunits` | body | `number` | yes | Minimum balance threshold in smallest currency unit. |
| `targetBalanceSubunits` | body | `number` | yes | Target balance in smallest currency unit. |
