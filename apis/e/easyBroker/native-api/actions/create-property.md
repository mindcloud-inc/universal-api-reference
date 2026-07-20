# Create Property with EasyBroker

Creates a new property in EasyBroker.

## Endpoint

- **Method:** `POST`
- **Path:** `/properties`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Create Property](https://dev.easybroker.com/reference/post_properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_type` | body | `string` | yes | Property type exactly as registered in EasyBroker. |
| `operations[0].type` | body | `string` | yes | Primary operation type, for example sale or rental. |
| `operations[0].amount` | body | `number` | yes | Primary operation amount. |
| `title` | body | `string` | yes | Property title. |
| `description` | body | `string` | yes | Property description. |
| `status` | body | `string` | yes | Property status, recommended not_published for initial creation. |
| `street` | body | `string` | yes | Property street. |
| `location.name` | body | `string` | yes | Location name matching EasyBroker location data. |
