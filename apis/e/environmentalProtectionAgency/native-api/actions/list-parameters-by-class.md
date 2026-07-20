# List Parameters By Class with Environmental Protection Agency

Retrieves parameters for a class from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/parametersByClass`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [List Parameters By Class](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pc` | query | `string` | yes | AQS parameter class name. Use ALL for every parameter class or a class returned by List Parameter Classes. |
