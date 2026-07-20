# Delete Custom Routing Profile with GraphHopper

Deletes a custom routing profile from GraphHopper.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/profiles/:profileId`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Delete Custom Routing Profile](https://docs.graphhopper.com/openapi/custom-profiles/deleteprofilesprofileid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Custom routing profile ID to delete. |
