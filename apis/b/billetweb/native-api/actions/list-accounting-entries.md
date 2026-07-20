# List Accounting Entries with Billetweb

Retrieves accounting entries from your Billetweb account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Accounting Entries](https://www.billetweb.fr/bo/api.php#/api/accounting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | Return entries modified after this Unix timestamp. |
| `end` | query | `number` | no | Optionally return entries modified before this Unix timestamp. |
| `canal` | query | `string` | no | Optionally limit results to web sales (web) or offline sales (other). |
| `event` | query | `number` | no | Optionally filter to a specific event id. |
