# Toggle Alerts with Vouchsafe

Updates ongoing monitoring for an alert account in Vouchsafe.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/alerts/accounts/:id`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Toggle Alerts](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The monitored account ID (Smart Lookup ID). |
| `alerts_enabled` | body | `boolean` | yes | Whether to enable or disable ongoing monitoring for this account. |
