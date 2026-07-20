# Get Charge KWh Consumption with Monta

Retrieves charge consumption breakdowns from Monta.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/{chargeId}/kwh-consumption`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [Get Charge KWh Consumption](https://docs.public-api.monta.com/reference/get-charge-kwh-consumption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargeId` | path | `number` | yes | ID of the charge to retrieve kWh consumption for. |
| `consumptionPeriodSizeInSeconds` | query | `list<number>` | no | Consumption interval size in seconds. Supported values are 3600, 1800, 900, 600, and 300. Accepted values: `1800`, `300`, `3600`, `600`, `900`. |
