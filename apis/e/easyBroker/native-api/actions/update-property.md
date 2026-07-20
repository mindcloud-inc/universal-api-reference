# Update Property with EasyBroker

Updates an existing property in EasyBroker.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/properties/{property_id}`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Update Property](https://dev.easybroker.com/reference/patch_properties-property-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_id` | path | `string` | yes | Internal or EasyBroker property ID. |
| `title` | body | `string` | no | Updated property title. |
| `status` | body | `string` | no | Updated property status. |
