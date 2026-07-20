# Transfer Credits to Subaccount with Seven

Creates a subaccount credit transfer in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/subaccounts?action=transfer_credits`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Transfer Credits to Subaccount](https://docs.seven.io/en/rest-api/endpoints/subaccounts#manual-credit-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the subaccount. |
| `amount` | body | `number` | yes | Credit to be transferred. |
