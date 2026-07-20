# Update Automatic Balance Transfer with Seven

Updates automatic balance transfer in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/subaccounts?action=update`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Update Automatic Balance Transfer](https://docs.seven.io/en/rest-api/endpoints/subaccounts#automatic-balance-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The ID of the subaccount. |
| `threshold` | body | `number` | yes | The credit threshold, below which credit should be transferred. |
| `amount` | body | `number` | yes | The amount of credit that should be sent from the main account to the subaccount when threshold is reached. |
