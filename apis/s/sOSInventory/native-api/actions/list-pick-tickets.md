# List Pick Tickets with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/pickticket`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Pick Tickets](https://developer.sosinventory.com/apidoc/PickTicket)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match pick ticket number, comment, customer, or location. |
| `status` | query | `list<string>` | no | Accepted values: `closed`, `open`. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `location` | query | `list<string>` | no | — |
| `channel` | query | `string` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
| `summary` | query | `string` | no | Any supplied value returns summary fields only. Leave empty for complete records. |
