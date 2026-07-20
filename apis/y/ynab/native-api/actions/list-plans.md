# List Plans with YNAB

Retrieves plans from YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Plans](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_accounts` | query | `boolean` | no | Whether to include the list of plan accounts. |
