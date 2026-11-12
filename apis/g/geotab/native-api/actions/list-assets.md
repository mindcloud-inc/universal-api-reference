# List Assets with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [List Assets](https://developers.geotab.com/myGeotab/apiReference/methods/Get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `object` | no | Optional DeviceSearch object. Supports fields such as id, deviceIds, name, serialNumber, vehicleIdentificationNumber, licensePlate, groups, fromDate, and toDate. |
| `resultsLimit` | body | `number` | no | Maximum assets to return. Device Get supports up to 5,000 results. |
| `sort` | body | `object` | no | Optional MyGeotab sort object. Device supports sorting by id or name. |
| `propertySelector` | body | `object` | no | Optional property selector used to include or exclude Device fields. |
