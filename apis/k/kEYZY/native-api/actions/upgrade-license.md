# Upgrade License with KEYZY

Upgrades a KEYZY license from another license.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/upgrade`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Upgrade License](https://www.keyzy.io/docs/developers/rest-api/licenses-upgrade/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_serial` | body | `string` | yes | Current license serial number. |
| `upgrade_serial` | body | `string` | yes | Upgrade license serial number. |
