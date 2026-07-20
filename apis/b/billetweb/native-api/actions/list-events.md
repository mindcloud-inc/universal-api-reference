# List Events with Billetweb

Retrieves events from your Billetweb account.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Events](https://www.billetweb.fr/bo/api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `past` | query | `boolean` | no | Include past events in the response. |
| `online` | query | `boolean` | no | Include only published online events. |
| `description` | query | `boolean` | no | Include the event description in the response. |
| `id` | query | `number` | no | Filter to one specific event ID. |
