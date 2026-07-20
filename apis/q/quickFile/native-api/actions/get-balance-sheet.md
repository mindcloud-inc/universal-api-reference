# Get Balance Sheet with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/report/balancesheet`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Get Balance Sheet](https://api.quickfile.co.uk/d/v1_2/Report_BalanceSheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ToDate` | body | `date` | no | Snapshot date for the balance sheet. |
| `ShowAsNBV` | body | `boolean` | no | When true, shows the balance sheet as net book value. |
