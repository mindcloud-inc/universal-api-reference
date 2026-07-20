# Create Project with CompanyCam

Creates a new project in CompanyCam.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Create Project](https://docs.companycam.com/reference/createproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.street_address_1` | body | `string` | no | — |
| `coordinates.lat` | body | `number` | no | between -3.402823669209385e+38 and 3.402823669209385e+38 |
| `geofence[].lat` | body | `number` | no | — |
| `name` | body | `string` | yes | — |
| `primaryContact.name` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `address.street_address_2` | body | `string` | no | — |
| `coordinates.lon` | body | `number` | no | between -3.402823669209385e+38 and 3.402823669209385e+38 Maximum length: 0. |
| `geofence[].lon` | body | `number` | no | — |
| `primaryContact.email` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `primary_contact` | body | `object` | no | — |
| `primary_contact.phone_number` | body | `string` | no | — |
| `address.state` | body | `string` | no | — |
| `coordinates` | body | `object` | no | — |
| `address.postal_code` | body | `string` | no | — |
| `geofence[]` | body | `array<object>` | no | (optional) Provide an array of multiple coordinates that effectively "draw" a shape around the address. The most common and easiest approach for a property is to draw a rectangular bounding box.  Below is an example geofence for a bounding box approximately 100 meters (330 feet) in each direction of these coordinates: (36.197441, -94.165699).  Geofence: 1. Top-Left (36.198441,-94.166699) 2. Top-Right (36.198441,-94.164699) 3. Bottom-Right (36.196441,-94.164699) 4. Bottom-Left (36.196441,-94.166699) |
| `address.country` | body | `string` | no | — |
