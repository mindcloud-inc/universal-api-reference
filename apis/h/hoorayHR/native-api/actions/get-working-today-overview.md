# Get Working Today Overview with HoorayHR

Retrieves a working today overview from HoorayHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/working-today`
- **Base URL:** `https://api.hoorayhr.io`
- **Official documentation:** [Get Working Today Overview](https://api.hoorayhr.io/documentation/#/working-today/findWorkingToday)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | The day to inspect in YYYY-MM-DD format. |
| `includeArchivedUsers` | query | `boolean` | no | Whether archived users should be included in the response. |
