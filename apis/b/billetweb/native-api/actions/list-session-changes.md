# List Session Changes with Billetweb

Retrieves session changes from your Billetweb account.

## Endpoint

- **Method:** `GET`
- **Path:** `/date_changes`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Session Changes](https://www.billetweb.fr/bo/api.php#/api/date_changes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | Return date change entries modified after this Unix timestamp. |
| `end` | query | `number` | no | Optionally return date change entries modified before this Unix timestamp. |
