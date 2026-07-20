# Get Company with FleetWire

Retrieves company details from FleetWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/company/:company`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [Get Company](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The FleetWire company UUID to fetch. |
| `include` | query | `string` | no | Comma-separated related resources to include, such as deliveryLocations,taxCategories,listings. |
