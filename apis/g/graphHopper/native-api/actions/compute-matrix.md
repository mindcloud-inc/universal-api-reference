# Compute Matrix with GraphHopper

Computes a route matrix in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/matrix`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Compute Matrix](https://docs.graphhopper.com/openapi/matrices/postmatrix)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Matrix request JSON body matching GraphHopper's MatrixRequest or SymmetricalMatrixRequest schema. |
