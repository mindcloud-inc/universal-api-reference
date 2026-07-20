# Create Manual Payout with Payrexx

Creates a manual payout in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Payout/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create Manual Payout](https://developers.payrexx.com/reference/create-manual-payout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pspId` | body | `number` | yes | Payout PSP id. |
| `amount` | body | `number` | yes | Payout amount in cents. |
| `currency` | body | `string` | yes | Payout currency. |
