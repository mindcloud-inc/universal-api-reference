# List Balances with NobelSMS

Retrieves balances from NobelSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/balance`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [List Balances](https://api.nobelsms.com/rest/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `car_id` | query | `number` | no | Carrier ID (for System owner users only). |
| `descr` | query | `string` | no | Account description filter. |
| `direction` | query | `number` | no | Account direction. |
