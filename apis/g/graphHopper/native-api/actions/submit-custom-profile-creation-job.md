# Submit Custom Profile Creation Job with GraphHopper

Submits a custom profile creation job in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles/calculate`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Submit Custom Profile Creation Job](https://docs.graphhopper.com/openapi/custom-profiles/postprofilescalculate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Asynchronous custom routing profile request JSON body matching GraphHopper's ProfileRequest schema. |
