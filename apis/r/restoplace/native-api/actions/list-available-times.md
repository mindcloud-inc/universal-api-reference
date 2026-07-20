# List Available Times with Restoplace

Retrieves available booking times from Restoplace.

## Endpoint

- **Method:** `GET`
- **Path:** `/times/`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [List Available Times](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Date to search for available times in YYYY-MM-DD format. |
| `length` | query | `number` | no | Reservation length in minutes. |
| `floorid` | query | `number` | no | Hall ID to search within. |
| `shift` | query | `string` | no | Optional shift selector supported by the provider. |
| `dateFormat` | query | `string` | no | Optional provider date format override. |
