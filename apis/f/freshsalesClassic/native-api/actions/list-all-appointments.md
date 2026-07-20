# List All Appointments with Freshsales Classic

Retrieves appointments from Freshsales Classic.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List All Appointments](https://developers.freshworks.com/crm/api/#list_all_appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | Freshsales appointment filter. Use one documented filter at a time: open or complete. |
| `page` | query | `number` | no | Page number to return. |
