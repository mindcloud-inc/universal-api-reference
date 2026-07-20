# Get Chart Of Accounts with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/report/chartofaccounts`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Get Chart Of Accounts](https://api.quickfile.co.uk/d/v1_2/Report_ChartOfAccounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StartNominalCode` | body | `number` | no | Starting nominal code for the chart of accounts range. |
| `EndNominalCode` | body | `number` | no | Ending nominal code for the chart of accounts range. |
| `FromDate` | body | `date` | no | Optional lower bound date for nominal balances. |
| `ToDate` | body | `date` | no | Optional upper bound date for nominal balances. |
| `ExcludeZeroBalanceLedgers` | body | `boolean` | no | When true, omits ledgers with a zero balance in the selected range. Defaults to false so the full chart of accounts is returned. |
| `ReturnCodeName` | body | `boolean` | no | When true, includes the nominal code name. |
| `ReturnDescription` | body | `boolean` | no | When true, includes the nominal code description. |
