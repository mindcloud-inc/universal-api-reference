# List Alert Accounts with Vouchsafe

Retrieves monitored alert accounts from Vouchsafe.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/accounts`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [List Alert Accounts](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Filter monitored accounts by alert status. Accepted values: `acknowledged`, `clear`, `new`. |
| `cursor` | query | `string` | no | Cursor for pagination using the ID of the last item from the previous page. |
