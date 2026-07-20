# Retrieve Partner Property with EasyBroker

Retrieves a property linked to your integration in EasyBroker.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration_partners/properties/:property_id`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Retrieve Partner Property](https://dev.easybroker.com/reference/get_properties-property-id-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_id` | path | `string` | yes | The EasyBroker property public ID. |
