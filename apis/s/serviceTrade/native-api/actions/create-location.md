# Create Location with ServiceTrade

Creates a new location in ServiceTrade.

## Endpoint

- **Method:** `POST`
- **Path:** `location`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Create Location](https://api.servicetrade.com/api/docs#resource-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `number` | yes | Company to attach the new location to. |
| `name` | body | `string` | yes | Name of the new location. |
| `addressStreet` | body | `string` | yes | Street address for the new location. |
| `addressCity` | body | `string` | yes | City for the new location. |
| `addressState` | body | `string` | yes | State or province for the new location. |
| `addressPostalCode` | body | `string` | yes | Postal code for the new location. |
