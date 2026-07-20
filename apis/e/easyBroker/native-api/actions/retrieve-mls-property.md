# Retrieve MLS Property with EasyBroker

Retrieves an MLS property from EasyBroker.

## Endpoint

- **Method:** `GET`
- **Path:** `/mls_properties/:property_id`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Retrieve MLS Property](https://dev.easybroker.com/reference/get_mls-properties-property-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_id` | path | `string` | yes | The public ID of the specified property. |
