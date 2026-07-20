# Get Tenancy Meter Readings with Alto

Retrieves tenancy meter readings from Alto.

## Endpoint

- **Method:** `GET`
- **Path:** `/tenancies/:tenancyId/meter-readings`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Tenancy Meter Readings](https://developers.vebraalto.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenancyId` | path | `string` | yes | Unique Alto tenancy identifier. |
