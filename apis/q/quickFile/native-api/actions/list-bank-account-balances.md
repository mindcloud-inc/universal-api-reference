# List Bank Account Balances with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/bank/getaccountbalances`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [List Bank Account Balances](https://api.quickfile.co.uk/d/v1_2/Bank_GetAccountBalances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `NominalCode` | body | `number` | yes | One or more QuickFile bank nominal codes to fetch balances for. Send multiple values as a array. |
