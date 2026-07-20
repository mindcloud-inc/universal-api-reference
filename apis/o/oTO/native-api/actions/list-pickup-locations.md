# List Pickup Locations with OTO

Retrieves pickup locations from the OTO API.

## Endpoint

- **Method:** `GET`
- **Path:** `/getPickupLocationList`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [List Pickup Locations](https://help.tryoto.com/en/support/solutions/articles/150000213814-pickup-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minDate` | query | `date` | yes | Earliest date to include when listing pickup locations, in YYYY-MM-DD format. |
