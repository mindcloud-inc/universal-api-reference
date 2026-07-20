# Submit Matrix Job with GraphHopper

Submits a matrix job in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/matrix/calculate`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Submit Matrix Job](https://docs.graphhopper.com/openapi/matrices/postmatrixcalculate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Asynchronous matrix request JSON body matching GraphHopper's MatrixRequest or SymmetricalMatrixRequest schema. |
