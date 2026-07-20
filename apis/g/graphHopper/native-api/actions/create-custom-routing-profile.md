# Create Custom Routing Profile with GraphHopper

Creates a custom routing profile in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Create Custom Routing Profile](https://docs.graphhopper.com/openapi/custom-profiles/postprofiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Custom routing profile request JSON body matching GraphHopper's ProfileRequest schema. |
